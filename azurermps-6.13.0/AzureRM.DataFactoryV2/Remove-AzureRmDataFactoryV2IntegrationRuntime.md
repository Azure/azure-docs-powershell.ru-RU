---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8c7ec74e43586a951b3f8d2c4d8af0caa6e09a2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556719"
---
# <span data-ttu-id="01e14-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="01e14-101">Remove-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="01e14-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01e14-102">SYNOPSIS</span></span>
<span data-ttu-id="01e14-103">Удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="01e14-103">Removes an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01e14-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01e14-104">SYNTAX</span></span>

### <span data-ttu-id="01e14-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="01e14-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e14-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="01e14-106">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01e14-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="01e14-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzureRmDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01e14-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01e14-108">DESCRIPTION</span></span>
<span data-ttu-id="01e14-109">Командлет Remove-AzureRmDataFactoryV2IntegrationRuntime удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="01e14-109">The Remove-AzureRmDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="01e14-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01e14-110">EXAMPLES</span></span>

### <span data-ttu-id="01e14-111">Пример 1: Удаление среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="01e14-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="01e14-112">Эта команда удаляет среду выполнения интеграции с именем "тест-зарезервирован-IR" из фабрики данных с именем "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="01e14-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="01e14-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="01e14-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="01e14-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01e14-114">PARAMETERS</span></span>

### <span data-ttu-id="01e14-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="01e14-115">-DataFactoryName</span></span>
<span data-ttu-id="01e14-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="01e14-116">The data factory name.</span></span>

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

### <span data-ttu-id="01e14-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01e14-117">-DefaultProfile</span></span>
<span data-ttu-id="01e14-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01e14-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01e14-119">-Force</span><span class="sxs-lookup"><span data-stu-id="01e14-119">-Force</span></span>
<span data-ttu-id="01e14-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="01e14-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="01e14-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01e14-121">-InputObject</span></span>
<span data-ttu-id="01e14-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="01e14-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="01e14-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="01e14-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="01e14-124">Имя связанной фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="01e14-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="01e14-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="01e14-125">-Name</span></span>
<span data-ttu-id="01e14-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="01e14-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="01e14-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01e14-127">-ResourceGroupName</span></span>
<span data-ttu-id="01e14-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="01e14-128">The resource group name.</span></span>

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

### <span data-ttu-id="01e14-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="01e14-129">-ResourceId</span></span>
<span data-ttu-id="01e14-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="01e14-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="01e14-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01e14-131">-Confirm</span></span>
<span data-ttu-id="01e14-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="01e14-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01e14-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01e14-133">-WhatIf</span></span>
<span data-ttu-id="01e14-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="01e14-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="01e14-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01e14-135">CommonParameters</span></span>
<span data-ttu-id="01e14-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01e14-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01e14-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01e14-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01e14-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01e14-138">INPUTS</span></span>

### <span data-ttu-id="01e14-139">System. String</span><span class="sxs-lookup"><span data-stu-id="01e14-139">System.String</span></span>

### <span data-ttu-id="01e14-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="01e14-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="01e14-141">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="01e14-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="01e14-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01e14-142">OUTPUTS</span></span>

### <span data-ttu-id="01e14-143">System. void</span><span class="sxs-lookup"><span data-stu-id="01e14-143">System.Void</span></span>

## <span data-ttu-id="01e14-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="01e14-144">NOTES</span></span>
<span data-ttu-id="01e14-145">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="01e14-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="01e14-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01e14-146">RELATED LINKS</span></span>

[<span data-ttu-id="01e14-147">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="01e14-147">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="01e14-148">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="01e14-148">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()


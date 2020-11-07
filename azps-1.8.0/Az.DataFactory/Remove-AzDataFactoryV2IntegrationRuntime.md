---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 9478c190d33608706006ff7fe792b4ee8f14b9d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900941"
---
# <span data-ttu-id="c0cca-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c0cca-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c0cca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0cca-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cca-103">Удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="c0cca-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="c0cca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0cca-104">SYNTAX</span></span>

### <span data-ttu-id="c0cca-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0cca-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0cca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c0cca-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0cca-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c0cca-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0cca-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0cca-108">DESCRIPTION</span></span>
<span data-ttu-id="c0cca-109">Командлет Remove-AzDataFactoryV2IntegrationRuntime удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="c0cca-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="c0cca-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0cca-110">EXAMPLES</span></span>

### <span data-ttu-id="c0cca-111">Пример 1: Удаление среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="c0cca-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="c0cca-112">Эта команда удаляет среду выполнения интеграции с именем "тест-зарезервирован-IR" из фабрики данных с именем "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="c0cca-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="c0cca-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="c0cca-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="c0cca-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0cca-114">PARAMETERS</span></span>

### <span data-ttu-id="c0cca-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c0cca-115">-DataFactoryName</span></span>
<span data-ttu-id="c0cca-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c0cca-116">The data factory name.</span></span>

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

### <span data-ttu-id="c0cca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cca-117">-DefaultProfile</span></span>
<span data-ttu-id="c0cca-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0cca-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0cca-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c0cca-119">-Force</span></span>
<span data-ttu-id="c0cca-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c0cca-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c0cca-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0cca-121">-InputObject</span></span>
<span data-ttu-id="c0cca-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="c0cca-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="c0cca-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="c0cca-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="c0cca-124">Имя связанной фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="c0cca-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="c0cca-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0cca-125">-Name</span></span>
<span data-ttu-id="c0cca-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="c0cca-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="c0cca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cca-127">-ResourceGroupName</span></span>
<span data-ttu-id="c0cca-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c0cca-128">The resource group name.</span></span>

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

### <span data-ttu-id="c0cca-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0cca-129">-ResourceId</span></span>
<span data-ttu-id="c0cca-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="c0cca-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c0cca-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0cca-131">-Confirm</span></span>
<span data-ttu-id="c0cca-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c0cca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0cca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0cca-133">-WhatIf</span></span>
<span data-ttu-id="c0cca-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="c0cca-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="c0cca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cca-135">CommonParameters</span></span>
<span data-ttu-id="c0cca-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0cca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cca-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0cca-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cca-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0cca-138">INPUTS</span></span>

### <span data-ttu-id="c0cca-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c0cca-139">System.String</span></span>

### <span data-ttu-id="c0cca-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c0cca-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c0cca-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0cca-141">OUTPUTS</span></span>

### <span data-ttu-id="c0cca-142">System. void</span><span class="sxs-lookup"><span data-stu-id="c0cca-142">System.Void</span></span>

## <span data-ttu-id="c0cca-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0cca-143">NOTES</span></span>
<span data-ttu-id="c0cca-144">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="c0cca-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="c0cca-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0cca-145">RELATED LINKS</span></span>

[<span data-ttu-id="c0cca-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c0cca-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="c0cca-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c0cca-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()


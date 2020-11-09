---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0c24f77b51bcfc50ec11e211fc7f11b60e348221
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313841"
---
# <span data-ttu-id="7e5ed-101">Remove-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7e5ed-101">Remove-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="7e5ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e5ed-102">SYNOPSIS</span></span>
<span data-ttu-id="7e5ed-103">Удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-103">Removes an integration runtime.</span></span>

## <span data-ttu-id="7e5ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e5ed-104">SYNTAX</span></span>

### <span data-ttu-id="7e5ed-105">ByIntegrationRuntimeName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7e5ed-105">ByIntegrationRuntimeName (Default)</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-Name] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e5ed-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7e5ed-106">ByResourceId</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e5ed-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="7e5ed-107">ByIntegrationRuntimeObject</span></span>
```
Remove-AzDataFactoryV2IntegrationRuntime [-LinkedDataFactoryName <String>] [-Force]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7e5ed-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e5ed-108">DESCRIPTION</span></span>
<span data-ttu-id="7e5ed-109">Командлет Remove-AzDataFactoryV2IntegrationRuntime удаляет среду выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-109">The Remove-AzDataFactoryV2IntegrationRuntime cmdlet removes a integration runtime.</span></span>

## <span data-ttu-id="7e5ed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e5ed-110">EXAMPLES</span></span>

### <span data-ttu-id="7e5ed-111">Пример 1: Удаление среды выполнения интеграции</span><span class="sxs-lookup"><span data-stu-id="7e5ed-111">Example 1: Remove a integration runtime</span></span>
```
PS C:\> Remove-AzDataFactoryV2IntegrationRuntime  -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df' -Name 'test-reserved-ir' -Confirm
```

<span data-ttu-id="7e5ed-112">Эта команда удаляет среду выполнения интеграции с именем "тест-зарезервирован-IR" из фабрики данных с именем "Test-DF".</span><span class="sxs-lookup"><span data-stu-id="7e5ed-112">This command removes the integration runtime named 'test-reserved-ir' from the data factory named 'test-df'.</span></span>
<span data-ttu-id="7e5ed-113">Эта команда возвращает значение $True.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="7e5ed-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e5ed-114">PARAMETERS</span></span>

### <span data-ttu-id="7e5ed-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7e5ed-115">-DataFactoryName</span></span>
<span data-ttu-id="7e5ed-116">Имя фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-116">The data factory name.</span></span>

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

### <span data-ttu-id="7e5ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e5ed-117">-DefaultProfile</span></span>
<span data-ttu-id="7e5ed-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e5ed-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7e5ed-119">-Force</span></span>
<span data-ttu-id="7e5ed-120">Запускает командлет без запроса на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-120">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="7e5ed-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e5ed-121">-InputObject</span></span>
<span data-ttu-id="7e5ed-122">Объект среды выполнения Integration.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-122">The integration runtime object.</span></span>

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

### <span data-ttu-id="7e5ed-123">-LinkedDataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7e5ed-123">-LinkedDataFactoryName</span></span>
<span data-ttu-id="7e5ed-124">Имя связанной фабрики данных.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-124">The linked data factory name.</span></span>

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

### <span data-ttu-id="7e5ed-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7e5ed-125">-Name</span></span>
<span data-ttu-id="7e5ed-126">Имя среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-126">The integration runtime name.</span></span>

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

### <span data-ttu-id="7e5ed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e5ed-127">-ResourceGroupName</span></span>
<span data-ttu-id="7e5ed-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-128">The resource group name.</span></span>

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

### <span data-ttu-id="7e5ed-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e5ed-129">-ResourceId</span></span>
<span data-ttu-id="7e5ed-130">Идентификатор ресурса Azure.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-130">The Azure resource ID.</span></span>

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

### <span data-ttu-id="7e5ed-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e5ed-131">-Confirm</span></span>
<span data-ttu-id="7e5ed-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e5ed-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e5ed-133">-WhatIf</span></span>
<span data-ttu-id="7e5ed-134">Показано, что происходит при запуске командлета, но не запускает командлет.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-134">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="7e5ed-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e5ed-135">CommonParameters</span></span>
<span data-ttu-id="7e5ed-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e5ed-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e5ed-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e5ed-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e5ed-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e5ed-138">INPUTS</span></span>

### <span data-ttu-id="7e5ed-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7e5ed-139">System.String</span></span>

### <span data-ttu-id="7e5ed-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7e5ed-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="7e5ed-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e5ed-141">OUTPUTS</span></span>

### <span data-ttu-id="7e5ed-142">System. void</span><span class="sxs-lookup"><span data-stu-id="7e5ed-142">System.Void</span></span>

## <span data-ttu-id="7e5ed-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e5ed-143">NOTES</span></span>
<span data-ttu-id="7e5ed-144">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Data, фабрики, копия, действия, интеграционная среда выполнения</span><span class="sxs-lookup"><span data-stu-id="7e5ed-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="7e5ed-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e5ed-145">RELATED LINKS</span></span>

[<span data-ttu-id="7e5ed-146">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7e5ed-146">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()

[<span data-ttu-id="7e5ed-147">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="7e5ed-147">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()


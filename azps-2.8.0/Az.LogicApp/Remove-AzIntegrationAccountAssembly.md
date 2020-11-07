---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAssembly.md
ms.openlocfilehash: ce3a3ae24a1064e036bc66e0fa7bfdaa6c74e0c5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720504"
---
# <span data-ttu-id="e6f2a-101">Remove-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e6f2a-101">Remove-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="e6f2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="e6f2a-103">Удаляет сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-103">Removes an integration account assembly.</span></span>

## <span data-ttu-id="e6f2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6f2a-104">SYNTAX</span></span>

### <span data-ttu-id="e6f2a-105">ByIntegrationAccount (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6f2a-105">ByIntegrationAccount (Default)</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f2a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e6f2a-106">ByInputObject</span></span>
```
Remove-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6f2a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f2a-107">ByResourceId</span></span>
```
Remove-AzIntegrationAccountAssembly -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6f2a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6f2a-108">DESCRIPTION</span></span>
<span data-ttu-id="e6f2a-109">Командлет **Remove-AzIntegrationAccountAssembly** удаляет сборку из учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-109">The **Remove-AzIntegrationAccountAssembly** cmdlet removes an assembly from an integration account.</span></span>

## <span data-ttu-id="e6f2a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6f2a-110">EXAMPLES</span></span>

### <span data-ttu-id="e6f2a-111">Пример 1: удаление сборки с помощью параметров</span><span class="sxs-lookup"><span data-stu-id="e6f2a-111">Example 1: Remove an assembly by parameters</span></span>
```powershell
PS C:\> Remove-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"
```

<span data-ttu-id="e6f2a-112">Удаляет сборку с именем "sampleAssembly", расположенную в учетной записи интеграции "sampleIntegrationAccount".</span><span class="sxs-lookup"><span data-stu-id="e6f2a-112">Removes the assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount".</span></span>

## <span data-ttu-id="e6f2a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6f2a-113">PARAMETERS</span></span>

### <span data-ttu-id="e6f2a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6f2a-114">-DefaultProfile</span></span>
<span data-ttu-id="e6f2a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6f2a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6f2a-116">-InputObject</span></span>
<span data-ttu-id="e6f2a-117">Сборка учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-117">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f2a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6f2a-118">-Name</span></span>
<span data-ttu-id="e6f2a-119">Имя сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f2a-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="e6f2a-120">-ParentName</span></span>
<span data-ttu-id="e6f2a-121">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f2a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6f2a-122">-PassThru</span></span>
<span data-ttu-id="e6f2a-123">Возвращает значение, указывающее, была ли команда успешной.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-123">Return whether the command was successful or not.</span></span>

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

### <span data-ttu-id="e6f2a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6f2a-124">-ResourceGroupName</span></span>
<span data-ttu-id="e6f2a-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6f2a-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6f2a-126">-ResourceId</span></span>
<span data-ttu-id="e6f2a-127">Идентификатор ресурса сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-127">The integration account assembly resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6f2a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6f2a-128">-Confirm</span></span>
<span data-ttu-id="e6f2a-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6f2a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6f2a-130">-WhatIf</span></span>
<span data-ttu-id="e6f2a-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e6f2a-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6f2a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6f2a-133">CommonParameters</span></span>
<span data-ttu-id="e6f2a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6f2a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6f2a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6f2a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6f2a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6f2a-136">INPUTS</span></span>

### <span data-ttu-id="e6f2a-137">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e6f2a-137">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="e6f2a-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e6f2a-138">System.String</span></span>

## <span data-ttu-id="e6f2a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6f2a-139">OUTPUTS</span></span>

### <span data-ttu-id="e6f2a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e6f2a-140">System.Boolean</span></span>

## <span data-ttu-id="e6f2a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6f2a-141">NOTES</span></span>

## <span data-ttu-id="e6f2a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6f2a-142">RELATED LINKS</span></span>

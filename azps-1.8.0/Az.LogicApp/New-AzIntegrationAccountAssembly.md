---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 41f2e9c99c219ce34eee8ad4a0fde9b63616b7f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899926"
---
# <span data-ttu-id="e3b2f-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e3b2f-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="e3b2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b2f-103">Создание сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="e3b2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3b2f-104">SYNTAX</span></span>

### <span data-ttu-id="e3b2f-105">ByIntegrationAccountAndFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3b2f-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b2f-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e3b2f-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3b2f-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e3b2f-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e3b2f-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e3b2f-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b2f-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e3b2f-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b2f-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e3b2f-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b2f-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e3b2f-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b2f-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e3b2f-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3b2f-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e3b2f-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3b2f-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3b2f-114">DESCRIPTION</span></span>
<span data-ttu-id="e3b2f-115">Командлет **Get-AzIntegrationAccountAssembly** создает новую сборку в учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="e3b2f-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3b2f-116">EXAMPLES</span></span>

### <span data-ttu-id="e3b2f-117">Пример 1: создание новой сборки с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="e3b2f-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e3b2f-118">Создает новую сборку с использованием локального файла, расположенного в пути к файлу, который хранится в разделе "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="e3b2f-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="e3b2f-119">Пример 2: создание новой сборки с использованием байтовых данных</span><span class="sxs-lookup"><span data-stu-id="e3b2f-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e3b2f-120">Создает новую сборку, используя массив байтов, содержащийся в "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="e3b2f-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="e3b2f-121">Пример 3: создание новой сборки с помощью ссылки на контент</span><span class="sxs-lookup"><span data-stu-id="e3b2f-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e3b2f-122">Создает новую сборку с использованием байтовых данных, расположенных на URL-адресе "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="e3b2f-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="e3b2f-123">Это предлагаемый метод для создания сборок крупного размера.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="e3b2f-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3b2f-124">PARAMETERS</span></span>

### <span data-ttu-id="e3b2f-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="e3b2f-125">-AssemblyData</span></span>
<span data-ttu-id="e3b2f-126">Данные байт сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-126">The integration account assembly byte data.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: ByIntegrationAccountAndFileBytes, ByInputObjectAndFileBytes, ByResourceIdAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="e3b2f-127">-AssemblyFilePath</span></span>
<span data-ttu-id="e3b2f-128">Путь к файлу сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-128">The integration account assembly file path.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByInputObjectAndFilePath, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="e3b2f-129">-ContentLink</span></span>
<span data-ttu-id="e3b2f-130">Общедоступная ссылка на данные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-130">A publicly accessible link to the integration account assembly data.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndContentLink, ByInputObjectAndContentLink, ByResourceIdAndContentLink
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b2f-131">-DefaultProfile</span></span>
<span data-ttu-id="e3b2f-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b2f-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e3b2f-133">-Metadata</span></span>
<span data-ttu-id="e3b2f-134">Метаданные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-134">The integration account assembly metadata.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3b2f-135">-Name</span></span>
<span data-ttu-id="e3b2f-136">Имя сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-136">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="e3b2f-137">-ParentName</span></span>
<span data-ttu-id="e3b2f-138">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-138">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e3b2f-139">-ParentObject</span></span>
<span data-ttu-id="e3b2f-140">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-140">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e3b2f-141">-ParentResourceId</span></span>
<span data-ttu-id="e3b2f-142">Идентификатор ресурса для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-142">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdAndContentLink, ByResourceIdAndFileBytes, ByResourceIdAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3b2f-143">-ResourceGroupName</span></span>
<span data-ttu-id="e3b2f-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-144">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3b2f-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3b2f-145">-Confirm</span></span>
<span data-ttu-id="e3b2f-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3b2f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3b2f-147">-WhatIf</span></span>
<span data-ttu-id="e3b2f-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3b2f-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3b2f-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b2f-150">CommonParameters</span></span>
<span data-ttu-id="e3b2f-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3b2f-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b2f-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3b2f-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b2f-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3b2f-153">INPUTS</span></span>

### <span data-ttu-id="e3b2f-154">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e3b2f-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="e3b2f-155">System. String</span><span class="sxs-lookup"><span data-stu-id="e3b2f-155">System.String</span></span>

## <span data-ttu-id="e3b2f-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3b2f-156">OUTPUTS</span></span>

### <span data-ttu-id="e3b2f-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e3b2f-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="e3b2f-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3b2f-158">NOTES</span></span>

## <span data-ttu-id="e3b2f-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3b2f-159">RELATED LINKS</span></span>

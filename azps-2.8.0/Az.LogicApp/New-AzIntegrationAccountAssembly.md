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
ms.locfileid: "93720523"
---
# <span data-ttu-id="d7d34-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d7d34-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d7d34-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d7d34-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d34-103">Создание сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="d7d34-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d7d34-104">SYNTAX</span></span>

### <span data-ttu-id="d7d34-105">ByIntegrationAccountAndFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d7d34-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7d34-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="d7d34-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7d34-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="d7d34-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d7d34-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="d7d34-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7d34-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="d7d34-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7d34-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="d7d34-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7d34-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="d7d34-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7d34-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="d7d34-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d7d34-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="d7d34-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d34-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d34-114">DESCRIPTION</span></span>
<span data-ttu-id="d7d34-115">Командлет **Get-AzIntegrationAccountAssembly** создает новую сборку в учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="d7d34-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d7d34-116">EXAMPLES</span></span>

### <span data-ttu-id="d7d34-117">Пример 1: создание новой сборки с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="d7d34-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d7d34-118">Создает новую сборку с использованием локального файла, расположенного в пути к файлу, который хранится в разделе "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="d7d34-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="d7d34-119">Пример 2: создание новой сборки с использованием байтовых данных</span><span class="sxs-lookup"><span data-stu-id="d7d34-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d7d34-120">Создает новую сборку, используя массив байтов, содержащийся в "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="d7d34-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="d7d34-121">Пример 3: создание новой сборки с помощью ссылки на контент</span><span class="sxs-lookup"><span data-stu-id="d7d34-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="d7d34-122">Создает новую сборку с использованием байтовых данных, расположенных на URL-адресе "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="d7d34-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="d7d34-123">Это предлагаемый метод для создания сборок крупного размера.</span><span class="sxs-lookup"><span data-stu-id="d7d34-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="d7d34-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d7d34-124">PARAMETERS</span></span>

### <span data-ttu-id="d7d34-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="d7d34-125">-AssemblyData</span></span>
<span data-ttu-id="d7d34-126">Данные байт сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="d7d34-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="d7d34-127">-AssemblyFilePath</span></span>
<span data-ttu-id="d7d34-128">Путь к файлу сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="d7d34-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="d7d34-129">-ContentLink</span></span>
<span data-ttu-id="d7d34-130">Общедоступная ссылка на данные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="d7d34-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d34-131">-DefaultProfile</span></span>
<span data-ttu-id="d7d34-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d34-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7d34-133">-Metadata</span><span class="sxs-lookup"><span data-stu-id="d7d34-133">-Metadata</span></span>
<span data-ttu-id="d7d34-134">Метаданные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="d7d34-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d7d34-135">-Name</span></span>
<span data-ttu-id="d7d34-136">Имя сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="d7d34-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="d7d34-137">-ParentName</span></span>
<span data-ttu-id="d7d34-138">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-138">The integration account name.</span></span>

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

### <span data-ttu-id="d7d34-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d7d34-139">-ParentObject</span></span>
<span data-ttu-id="d7d34-140">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-140">An integration account object.</span></span>

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

### <span data-ttu-id="d7d34-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d7d34-141">-ParentResourceId</span></span>
<span data-ttu-id="d7d34-142">Идентификатор ресурса для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="d7d34-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="d7d34-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d34-143">-ResourceGroupName</span></span>
<span data-ttu-id="d7d34-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d7d34-144">The resource group name.</span></span>

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

### <span data-ttu-id="d7d34-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7d34-145">-Confirm</span></span>
<span data-ttu-id="d7d34-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d7d34-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d34-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d34-147">-WhatIf</span></span>
<span data-ttu-id="d7d34-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d7d34-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7d34-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d7d34-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d34-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d34-150">CommonParameters</span></span>
<span data-ttu-id="d7d34-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d7d34-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d34-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d34-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d34-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d7d34-153">INPUTS</span></span>

### <span data-ttu-id="d7d34-154">Microsoft. Azure. Management. Logic. Models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="d7d34-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="d7d34-155">System. String</span><span class="sxs-lookup"><span data-stu-id="d7d34-155">System.String</span></span>

## <span data-ttu-id="d7d34-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d7d34-156">OUTPUTS</span></span>

### <span data-ttu-id="d7d34-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="d7d34-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="d7d34-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="d7d34-158">NOTES</span></span>

## <span data-ttu-id="d7d34-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d7d34-159">RELATED LINKS</span></span>

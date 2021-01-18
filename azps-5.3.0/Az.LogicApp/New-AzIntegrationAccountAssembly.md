---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504710"
---
# <span data-ttu-id="e21dc-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e21dc-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="e21dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e21dc-102">SYNOPSIS</span></span>
<span data-ttu-id="e21dc-103">Создает сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e21dc-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="e21dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e21dc-104">SYNTAX</span></span>

### <span data-ttu-id="e21dc-105">ByIntegrationAccountAndFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e21dc-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21dc-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e21dc-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e21dc-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e21dc-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e21dc-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e21dc-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21dc-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e21dc-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21dc-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e21dc-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21dc-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="e21dc-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21dc-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="e21dc-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e21dc-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="e21dc-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e21dc-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e21dc-114">DESCRIPTION</span></span>
<span data-ttu-id="e21dc-115">С **его учетной записью в** учетной записи интеграции создается новая сборка.</span><span class="sxs-lookup"><span data-stu-id="e21dc-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="e21dc-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e21dc-116">EXAMPLES</span></span>

### <span data-ttu-id="e21dc-117">Пример 1. Создание сборки с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="e21dc-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e21dc-118">Создает сборку, используя локальный файл, расположенный по пути к файлу, который содержится в $localAssemblyFilePath.</span><span class="sxs-lookup"><span data-stu-id="e21dc-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="e21dc-119">Пример 2. Создание сборки с использованием byte data</span><span class="sxs-lookup"><span data-stu-id="e21dc-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e21dc-120">Создает сборку, используя массив, содержащийся в $assemblyContent.</span><span class="sxs-lookup"><span data-stu-id="e21dc-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="e21dc-121">Пример 3. Создание сборки с помощью ссылки на содержимое</span><span class="sxs-lookup"><span data-stu-id="e21dc-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="e21dc-122">Создает сборку на личные данные, расположенные по URL-адресу "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="e21dc-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="e21dc-123">Это рекомендуемый способ создания сборок больших размеров.</span><span class="sxs-lookup"><span data-stu-id="e21dc-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="e21dc-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e21dc-124">PARAMETERS</span></span>

### <span data-ttu-id="e21dc-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="e21dc-125">-AssemblyData</span></span>
<span data-ttu-id="e21dc-126">Сборка byte учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e21dc-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="e21dc-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="e21dc-127">-AssemblyFilePath</span></span>
<span data-ttu-id="e21dc-128">Путь к файлу сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e21dc-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="e21dc-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="e21dc-129">-ContentLink</span></span>
<span data-ttu-id="e21dc-130">Ссылка на сборку учетной записи интеграции, доступная всем.</span><span class="sxs-lookup"><span data-stu-id="e21dc-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="e21dc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e21dc-131">-DefaultProfile</span></span>
<span data-ttu-id="e21dc-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e21dc-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e21dc-133">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="e21dc-133">-Metadata</span></span>
<span data-ttu-id="e21dc-134">Метаданные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e21dc-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="e21dc-135">-Name</span><span class="sxs-lookup"><span data-stu-id="e21dc-135">-Name</span></span>
<span data-ttu-id="e21dc-136">Имя сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e21dc-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="e21dc-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="e21dc-137">-ParentName</span></span>
<span data-ttu-id="e21dc-138">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e21dc-138">The integration account name.</span></span>

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

### <span data-ttu-id="e21dc-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="e21dc-139">-ParentObject</span></span>
<span data-ttu-id="e21dc-140">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e21dc-140">An integration account object.</span></span>

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

### <span data-ttu-id="e21dc-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="e21dc-141">-ParentResourceId</span></span>
<span data-ttu-id="e21dc-142">ИД ресурса учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="e21dc-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="e21dc-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e21dc-143">-ResourceGroupName</span></span>
<span data-ttu-id="e21dc-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e21dc-144">The resource group name.</span></span>

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

### <span data-ttu-id="e21dc-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e21dc-145">-Confirm</span></span>
<span data-ttu-id="e21dc-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e21dc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e21dc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e21dc-147">-WhatIf</span></span>
<span data-ttu-id="e21dc-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e21dc-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e21dc-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e21dc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e21dc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e21dc-150">CommonParameters</span></span>
<span data-ttu-id="e21dc-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e21dc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e21dc-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e21dc-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e21dc-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e21dc-153">INPUTS</span></span>

### <span data-ttu-id="e21dc-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="e21dc-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="e21dc-155">System.String</span><span class="sxs-lookup"><span data-stu-id="e21dc-155">System.String</span></span>

## <span data-ttu-id="e21dc-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e21dc-156">OUTPUTS</span></span>

### <span data-ttu-id="e21dc-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="e21dc-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="e21dc-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e21dc-158">NOTES</span></span>

## <span data-ttu-id="e21dc-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e21dc-159">RELATED LINKS</span></span>

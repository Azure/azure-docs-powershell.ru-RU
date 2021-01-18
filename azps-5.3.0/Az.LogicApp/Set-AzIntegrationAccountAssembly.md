---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505104"
---
# <span data-ttu-id="f53fc-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f53fc-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="f53fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f53fc-102">SYNOPSIS</span></span>
<span data-ttu-id="f53fc-103">Изменяет сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="f53fc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f53fc-104">SYNTAX</span></span>

### <span data-ttu-id="f53fc-105">ByIntegrationAccountAndFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f53fc-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fc-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f53fc-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f53fc-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f53fc-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f53fc-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f53fc-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fc-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f53fc-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fc-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="f53fc-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fc-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="f53fc-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fc-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="f53fc-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f53fc-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="f53fc-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f53fc-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f53fc-114">DESCRIPTION</span></span>
<span data-ttu-id="f53fc-115">**Cmdlet Set-AzIntegrationAccountAssembly** изменяет сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="f53fc-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f53fc-116">EXAMPLES</span></span>

### <span data-ttu-id="f53fc-117">Пример 1. Изменение сборки с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="f53fc-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f53fc-118">Изменяет сборку sampleAssembly, используя локальный файл, расположенный по пути к файлу, который содержится в $localAssemblyFilePath.</span><span class="sxs-lookup"><span data-stu-id="f53fc-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="f53fc-119">Пример 2. Изменение сборки с использованием byte data</span><span class="sxs-lookup"><span data-stu-id="f53fc-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f53fc-120">Изменяет сборку sampleAssembly, используя массив, содержащийся в $assemblyContent.</span><span class="sxs-lookup"><span data-stu-id="f53fc-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="f53fc-121">Пример 3. Изменение сборки с помощью ссылки на содержимое</span><span class="sxs-lookup"><span data-stu-id="f53fc-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="f53fc-122">Изменяет сборку sampleAssembly, используя данные, расположенные по URL-адресу "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="f53fc-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="f53fc-123">Это рекомендуемый способ создания сборок больших размеров.</span><span class="sxs-lookup"><span data-stu-id="f53fc-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="f53fc-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f53fc-124">PARAMETERS</span></span>

### <span data-ttu-id="f53fc-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="f53fc-125">-AssemblyData</span></span>
<span data-ttu-id="f53fc-126">Сборка byte учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="f53fc-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="f53fc-127">-AssemblyFilePath</span></span>
<span data-ttu-id="f53fc-128">Путь к файлу сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="f53fc-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="f53fc-129">-ContentLink</span></span>
<span data-ttu-id="f53fc-130">Ссылка на сборку учетной записи интеграции, доступная всем.</span><span class="sxs-lookup"><span data-stu-id="f53fc-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="f53fc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f53fc-131">-DefaultProfile</span></span>
<span data-ttu-id="f53fc-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f53fc-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f53fc-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f53fc-133">-InputObject</span></span>
<span data-ttu-id="f53fc-134">Сборка учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-134">An integration account assembly.</span></span>

```yaml
Type: Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly
Parameter Sets: ByInputObjectAndContentLink, ByInputObjectAndFileBytes, ByInputObjectAndFilePath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f53fc-135">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="f53fc-135">-Metadata</span></span>
<span data-ttu-id="f53fc-136">Метаданные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="f53fc-137">-Name</span><span class="sxs-lookup"><span data-stu-id="f53fc-137">-Name</span></span>
<span data-ttu-id="f53fc-138">Имя сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-138">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccountAndFilePath, ByIntegrationAccountAndContentLink, ByIntegrationAccountAndFileBytes
Aliases: AssemblyName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f53fc-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="f53fc-139">-ParentName</span></span>
<span data-ttu-id="f53fc-140">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-140">The integration account name.</span></span>

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

### <span data-ttu-id="f53fc-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f53fc-141">-ResourceGroupName</span></span>
<span data-ttu-id="f53fc-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f53fc-142">The resource group name.</span></span>

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

### <span data-ttu-id="f53fc-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f53fc-143">-ResourceId</span></span>
<span data-ttu-id="f53fc-144">ID ресурса сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="f53fc-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="f53fc-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f53fc-145">-Confirm</span></span>
<span data-ttu-id="f53fc-146">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f53fc-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f53fc-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f53fc-147">-WhatIf</span></span>
<span data-ttu-id="f53fc-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f53fc-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f53fc-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f53fc-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f53fc-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f53fc-150">CommonParameters</span></span>
<span data-ttu-id="f53fc-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f53fc-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f53fc-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f53fc-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f53fc-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f53fc-153">INPUTS</span></span>

### <span data-ttu-id="f53fc-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f53fc-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="f53fc-155">System.String</span><span class="sxs-lookup"><span data-stu-id="f53fc-155">System.String</span></span>

## <span data-ttu-id="f53fc-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f53fc-156">OUTPUTS</span></span>

### <span data-ttu-id="f53fc-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="f53fc-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="f53fc-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f53fc-158">NOTES</span></span>

## <span data-ttu-id="f53fc-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f53fc-159">RELATED LINKS</span></span>

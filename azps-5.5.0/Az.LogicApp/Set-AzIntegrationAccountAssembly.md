---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224385"
---
# <span data-ttu-id="a7168-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a7168-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="a7168-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7168-102">SYNOPSIS</span></span>
<span data-ttu-id="a7168-103">Изменяет сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="a7168-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7168-104">SYNTAX</span></span>

### <span data-ttu-id="a7168-105">ByIntegrationAccountAndFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7168-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7168-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="a7168-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7168-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="a7168-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a7168-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="a7168-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7168-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="a7168-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7168-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a7168-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7168-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="a7168-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7168-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="a7168-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7168-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="a7168-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7168-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7168-114">DESCRIPTION</span></span>
<span data-ttu-id="a7168-115">**Cmdlet Set-AzIntegrationAccountAssembly** изменяет сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="a7168-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7168-116">EXAMPLES</span></span>

### <span data-ttu-id="a7168-117">Пример 1. Изменение сборки с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="a7168-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a7168-118">Изменяет сборку sampleAssembly, используя локальный файл, расположенный по пути к файлу, который содержится в $localAssemblyFilePath.</span><span class="sxs-lookup"><span data-stu-id="a7168-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="a7168-119">Пример 2. Изменение сборки с помощью byte data</span><span class="sxs-lookup"><span data-stu-id="a7168-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a7168-120">Изменяет сборку sampleAssembly, используя массив, содержащийся в $assemblyContent.</span><span class="sxs-lookup"><span data-stu-id="a7168-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="a7168-121">Пример 3. Изменение сборки с помощью ссылки на содержимое</span><span class="sxs-lookup"><span data-stu-id="a7168-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a7168-122">Изменяет сборку sampleAssembly, используя данные, расположенные по URL-адресу "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="a7168-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="a7168-123">Это рекомендуемый способ создания сборок больших размеров.</span><span class="sxs-lookup"><span data-stu-id="a7168-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="a7168-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7168-124">PARAMETERS</span></span>

### <span data-ttu-id="a7168-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="a7168-125">-AssemblyData</span></span>
<span data-ttu-id="a7168-126">Сборка byte учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="a7168-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="a7168-127">-AssemblyFilePath</span></span>
<span data-ttu-id="a7168-128">Путь к файлу сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="a7168-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="a7168-129">-ContentLink</span></span>
<span data-ttu-id="a7168-130">Ссылка на сборку учетной записи интеграции, доступная всем.</span><span class="sxs-lookup"><span data-stu-id="a7168-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="a7168-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7168-131">-DefaultProfile</span></span>
<span data-ttu-id="a7168-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7168-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7168-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7168-133">-InputObject</span></span>
<span data-ttu-id="a7168-134">Сборка учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="a7168-135">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="a7168-135">-Metadata</span></span>
<span data-ttu-id="a7168-136">Метаданные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="a7168-137">-Name</span><span class="sxs-lookup"><span data-stu-id="a7168-137">-Name</span></span>
<span data-ttu-id="a7168-138">Имя сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="a7168-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="a7168-139">-ParentName</span></span>
<span data-ttu-id="a7168-140">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-140">The integration account name.</span></span>

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

### <span data-ttu-id="a7168-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7168-141">-ResourceGroupName</span></span>
<span data-ttu-id="a7168-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7168-142">The resource group name.</span></span>

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

### <span data-ttu-id="a7168-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7168-143">-ResourceId</span></span>
<span data-ttu-id="a7168-144">ID ресурса сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="a7168-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="a7168-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7168-145">-Confirm</span></span>
<span data-ttu-id="a7168-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7168-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7168-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7168-147">-WhatIf</span></span>
<span data-ttu-id="a7168-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7168-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7168-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7168-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7168-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7168-150">CommonParameters</span></span>
<span data-ttu-id="a7168-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7168-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7168-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7168-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7168-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7168-153">INPUTS</span></span>

### <span data-ttu-id="a7168-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a7168-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="a7168-155">System.String</span><span class="sxs-lookup"><span data-stu-id="a7168-155">System.String</span></span>

## <span data-ttu-id="a7168-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7168-156">OUTPUTS</span></span>

### <span data-ttu-id="a7168-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a7168-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="a7168-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7168-158">NOTES</span></span>

## <span data-ttu-id="a7168-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7168-159">RELATED LINKS</span></span>

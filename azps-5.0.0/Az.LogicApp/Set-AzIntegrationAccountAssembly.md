---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 44f44fab1cbdd5346bbda4e1271c8dbf33b0e9f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250129"
---
# <span data-ttu-id="70695-101">Set-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="70695-101">Set-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="70695-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70695-102">SYNOPSIS</span></span>
<span data-ttu-id="70695-103">Изменение сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-103">Modifies an integration account assembly.</span></span>

## <span data-ttu-id="70695-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70695-104">SYNTAX</span></span>

### <span data-ttu-id="70695-105">ByIntegrationAccountAndFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70695-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70695-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="70695-106">ByIntegrationAccountAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70695-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="70695-107">ByIntegrationAccountAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="70695-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="70695-108">ByInputObjectAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70695-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="70695-109">ByInputObjectAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70695-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="70695-110">ByInputObjectAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -InputObject <PSIntegrationAccountAssembly> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70695-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="70695-111">ByResourceIdAndContentLink</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -ContentLink <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70695-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="70695-112">ByResourceIdAndFileBytes</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyData <Byte[]> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70695-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="70695-113">ByResourceIdAndFilePath</span></span>
```
Set-AzIntegrationAccountAssembly -ResourceId <String> -AssemblyFilePath <String> [-Metadata <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70695-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70695-114">DESCRIPTION</span></span>
<span data-ttu-id="70695-115">Командлет **Set-AzIntegrationAccountAssembly** изменяет сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-115">The **Set-AzIntegrationAccountAssembly** cmdlet modifies an integration account assembly.</span></span>

## <span data-ttu-id="70695-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70695-116">EXAMPLES</span></span>

### <span data-ttu-id="70695-117">Пример 1: изменение сборки с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="70695-117">Example 1: Modify an assembly using local file</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="70695-118">Изменяет сборку с именем "sampleAssembly" с помощью локального файла, расположенного в пути к файлу, который хранится в разделе "$localAssemblyFilePath".</span><span class="sxs-lookup"><span data-stu-id="70695-118">Modifies the assembly named "sampleAssembly" using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="70695-119">Пример 2: изменение сборки с помощью байтовых данных</span><span class="sxs-lookup"><span data-stu-id="70695-119">Example 2: Modify an assembly using byte data</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="70695-120">Изменяет сборку с именем "sampleAssembly", используя массив байтов, содержащийся в "$assemblyContent".</span><span class="sxs-lookup"><span data-stu-id="70695-120">Modifies the assembly named "sampleAssembly" using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="70695-121">Пример 3: изменение сборки с помощью ссылки на контент</span><span class="sxs-lookup"><span data-stu-id="70695-121">Example 3: Modify an assembly using a content link</span></span>
```powershell
PS C:\> Set-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="70695-122">Изменяет сборку с именем "sampleAssembly", используя байтовые данные, расположенные по URL-адресу "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="70695-122">Modifies the assembly named "sampleAssembly" using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="70695-123">Это предлагаемый метод для создания сборок крупного размера.</span><span class="sxs-lookup"><span data-stu-id="70695-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="70695-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70695-124">PARAMETERS</span></span>

### <span data-ttu-id="70695-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="70695-125">-AssemblyData</span></span>
<span data-ttu-id="70695-126">Данные байт сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="70695-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="70695-127">-AssemblyFilePath</span></span>
<span data-ttu-id="70695-128">Путь к файлу сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="70695-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="70695-129">-ContentLink</span></span>
<span data-ttu-id="70695-130">Общедоступная ссылка на данные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="70695-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70695-131">-DefaultProfile</span></span>
<span data-ttu-id="70695-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70695-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="70695-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="70695-133">-InputObject</span></span>
<span data-ttu-id="70695-134">Сборка учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-134">An integration account assembly.</span></span>

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

### <span data-ttu-id="70695-135">-Metadata</span><span class="sxs-lookup"><span data-stu-id="70695-135">-Metadata</span></span>
<span data-ttu-id="70695-136">Метаданные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-136">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="70695-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70695-137">-Name</span></span>
<span data-ttu-id="70695-138">Имя сборки для учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-138">The integration account assembly name.</span></span>

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

### <span data-ttu-id="70695-139">-ParentName</span><span class="sxs-lookup"><span data-stu-id="70695-139">-ParentName</span></span>
<span data-ttu-id="70695-140">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-140">The integration account name.</span></span>

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

### <span data-ttu-id="70695-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70695-141">-ResourceGroupName</span></span>
<span data-ttu-id="70695-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70695-142">The resource group name.</span></span>

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

### <span data-ttu-id="70695-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="70695-143">-ResourceId</span></span>
<span data-ttu-id="70695-144">Идентификатор ресурса сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="70695-144">The integration account assembly resource id.</span></span>

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

### <span data-ttu-id="70695-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70695-145">-Confirm</span></span>
<span data-ttu-id="70695-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70695-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70695-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70695-147">-WhatIf</span></span>
<span data-ttu-id="70695-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70695-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70695-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70695-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70695-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70695-150">CommonParameters</span></span>
<span data-ttu-id="70695-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70695-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70695-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70695-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70695-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70695-153">INPUTS</span></span>

### <span data-ttu-id="70695-154">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="70695-154">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

### <span data-ttu-id="70695-155">System. String</span><span class="sxs-lookup"><span data-stu-id="70695-155">System.String</span></span>

## <span data-ttu-id="70695-156">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70695-156">OUTPUTS</span></span>

### <span data-ttu-id="70695-157">Microsoft. Azure. Commands. LogicApp. Models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="70695-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="70695-158">Пуск</span><span class="sxs-lookup"><span data-stu-id="70695-158">NOTES</span></span>

## <span data-ttu-id="70695-159">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70695-159">RELATED LINKS</span></span>

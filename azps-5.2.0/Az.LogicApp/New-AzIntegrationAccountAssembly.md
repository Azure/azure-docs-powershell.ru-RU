---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 0ea35e2f687308690107df5f92649dbbbeccdbaf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324172"
---
# <span data-ttu-id="3f024-101">New-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3f024-101">New-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="3f024-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f024-102">SYNOPSIS</span></span>
<span data-ttu-id="3f024-103">Создает сборку учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f024-103">Creates an integration account assembly.</span></span>

## <span data-ttu-id="3f024-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3f024-104">SYNTAX</span></span>

### <span data-ttu-id="3f024-105">ByIntegrationAccountAndFilePath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f024-105">ByIntegrationAccountAndFilePath (Default)</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyFilePath <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f024-106">ByIntegrationAccountAndContentLink</span><span class="sxs-lookup"><span data-stu-id="3f024-106">ByIntegrationAccountAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -ContentLink <String> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f024-107">ByIntegrationAccountAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="3f024-107">ByIntegrationAccountAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> -Name <String>
 -AssemblyData <Byte[]> [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f024-108">ByInputObjectAndContentLink</span><span class="sxs-lookup"><span data-stu-id="3f024-108">ByInputObjectAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f024-109">ByInputObjectAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="3f024-109">ByInputObjectAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f024-110">ByInputObjectAndFilePath</span><span class="sxs-lookup"><span data-stu-id="3f024-110">ByInputObjectAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f024-111">ByResourceIdAndContentLink</span><span class="sxs-lookup"><span data-stu-id="3f024-111">ByResourceIdAndContentLink</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -ContentLink <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f024-112">ByResourceIdAndFileBytes</span><span class="sxs-lookup"><span data-stu-id="3f024-112">ByResourceIdAndFileBytes</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyData <Byte[]>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f024-113">ByResourceIdAndFilePath</span><span class="sxs-lookup"><span data-stu-id="3f024-113">ByResourceIdAndFilePath</span></span>
```
New-AzIntegrationAccountAssembly -ParentResourceId <String> -Name <String> -AssemblyFilePath <String>
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f024-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f024-114">DESCRIPTION</span></span>
<span data-ttu-id="3f024-115">С **его учетной записью в** учетной записи интеграции создается новая сборка.</span><span class="sxs-lookup"><span data-stu-id="3f024-115">The **Get-AzIntegrationAccountAssembly** cmdlet creates a new assembly in an integration account.</span></span>

## <span data-ttu-id="3f024-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3f024-116">EXAMPLES</span></span>

### <span data-ttu-id="3f024-117">Пример 1. Создание сборки с помощью локального файла</span><span class="sxs-lookup"><span data-stu-id="3f024-117">Example 1: Create new assembly using local file</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyFilePath $localAssemblyFilePath

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="3f024-118">Создает сборку, используя локальный файл, расположенный по пути к файлу, который содержится в $localAssemblyFilePath.</span><span class="sxs-lookup"><span data-stu-id="3f024-118">Creates a new assembly using the local file located at the file path contained in "$localAssemblyFilePath".</span></span>

### <span data-ttu-id="3f024-119">Пример 2. Создание сборки с использованием byte data</span><span class="sxs-lookup"><span data-stu-id="3f024-119">Example 2: Create new assembly using byte data</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -AssemblyData $assemblyContent

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="3f024-120">Создает сборку, используя массив, содержащийся в $assemblyContent.</span><span class="sxs-lookup"><span data-stu-id="3f024-120">Creates a new assembly using the a byte array contained in "$assemblyContent".</span></span>

### <span data-ttu-id="3f024-121">Пример 3. Создание сборки с помощью ссылки на содержимое</span><span class="sxs-lookup"><span data-stu-id="3f024-121">Example 3: Create new assembly using a content link</span></span>
```powershell
PS C:\> New-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly" -ContentLink $assemblyUrl

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="3f024-122">Создает сборку с помощью byte-данных, расположенных по URL-адресу "$assemblyUrl".</span><span class="sxs-lookup"><span data-stu-id="3f024-122">Creates a new assembly using the a byte data located at the URL "$assemblyUrl".</span></span> <span data-ttu-id="3f024-123">Это рекомендуемый способ создания сборок больших размеров.</span><span class="sxs-lookup"><span data-stu-id="3f024-123">This is the suggested method for creating large sized assemblies.</span></span>

## <span data-ttu-id="3f024-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f024-124">PARAMETERS</span></span>

### <span data-ttu-id="3f024-125">-AssemblyData</span><span class="sxs-lookup"><span data-stu-id="3f024-125">-AssemblyData</span></span>
<span data-ttu-id="3f024-126">Сборка byte учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f024-126">The integration account assembly byte data.</span></span>

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

### <span data-ttu-id="3f024-127">-AssemblyFilePath</span><span class="sxs-lookup"><span data-stu-id="3f024-127">-AssemblyFilePath</span></span>
<span data-ttu-id="3f024-128">Путь к файлу сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f024-128">The integration account assembly file path.</span></span>

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

### <span data-ttu-id="3f024-129">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="3f024-129">-ContentLink</span></span>
<span data-ttu-id="3f024-130">Ссылка на сборку учетной записи интеграции, доступная всем.</span><span class="sxs-lookup"><span data-stu-id="3f024-130">A publicly accessible link to the integration account assembly data.</span></span>

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

### <span data-ttu-id="3f024-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f024-131">-DefaultProfile</span></span>
<span data-ttu-id="3f024-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f024-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f024-133">-Метаданные</span><span class="sxs-lookup"><span data-stu-id="3f024-133">-Metadata</span></span>
<span data-ttu-id="3f024-134">Метаданные сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f024-134">The integration account assembly metadata.</span></span>

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

### <span data-ttu-id="3f024-135">-Name</span><span class="sxs-lookup"><span data-stu-id="3f024-135">-Name</span></span>
<span data-ttu-id="3f024-136">Имя сборки учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f024-136">The integration account assembly name.</span></span>

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

### <span data-ttu-id="3f024-137">-ParentName</span><span class="sxs-lookup"><span data-stu-id="3f024-137">-ParentName</span></span>
<span data-ttu-id="3f024-138">Имя учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f024-138">The integration account name.</span></span>

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

### <span data-ttu-id="3f024-139">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="3f024-139">-ParentObject</span></span>
<span data-ttu-id="3f024-140">Объект учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f024-140">An integration account object.</span></span>

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

### <span data-ttu-id="3f024-141">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3f024-141">-ParentResourceId</span></span>
<span data-ttu-id="3f024-142">ИД ресурса учетной записи интеграции.</span><span class="sxs-lookup"><span data-stu-id="3f024-142">The integration account resource id.</span></span>

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

### <span data-ttu-id="3f024-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f024-143">-ResourceGroupName</span></span>
<span data-ttu-id="3f024-144">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f024-144">The resource group name.</span></span>

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

### <span data-ttu-id="3f024-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f024-145">-Confirm</span></span>
<span data-ttu-id="3f024-146">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f024-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f024-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f024-147">-WhatIf</span></span>
<span data-ttu-id="3f024-148">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f024-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f024-149">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3f024-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f024-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f024-150">CommonParameters</span></span>
<span data-ttu-id="3f024-151">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f024-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f024-152">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f024-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f024-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f024-153">INPUTS</span></span>

### <span data-ttu-id="3f024-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="3f024-154">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="3f024-155">System.String</span><span class="sxs-lookup"><span data-stu-id="3f024-155">System.String</span></span>

## <span data-ttu-id="3f024-156">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3f024-156">OUTPUTS</span></span>

### <span data-ttu-id="3f024-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="3f024-157">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="3f024-158">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3f024-158">NOTES</span></span>

## <span data-ttu-id="3f024-159">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f024-159">RELATED LINKS</span></span>

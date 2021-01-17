---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CC9D74BB-DFB2-41F3-B5CF-B265C549EC33
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 3036b02d280542ffa4c8eea85dafed2da8eb5e28
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418535"
---
# <span data-ttu-id="3d43c-101">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d43c-101">Import-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="3d43c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d43c-102">SYNOPSIS</span></span>
<span data-ttu-id="3d43c-103">Импортирует документ в качестве узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3d43c-103">Imports a MOF document as a DSC node configuration in Automation.</span></span>

## <span data-ttu-id="3d43c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3d43c-104">SYNTAX</span></span>

```
Import-AzAutomationDscNodeConfiguration -Path <String> -ConfigurationName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncrementNodeConfigurationBuild] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d43c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3d43c-105">DESCRIPTION</span></span>
<span data-ttu-id="3d43c-106">Cmdlet **Import-AzAutomationDscConfiguration** импортирует документ конфигурации "Управляемый формат объекта" (MOF) в автоматизацию Azure в качестве конфигурации узла DSC.</span><span class="sxs-lookup"><span data-stu-id="3d43c-106">The **Import-AzAutomationDscConfiguration** cmdlet imports a Managed Object Format (MOF) configuration document into Azure Automation as a Desired State Configuration (DSC) node configuration.</span></span>
<span data-ttu-id="3d43c-107">Укажите путь к MOF-файлу.</span><span class="sxs-lookup"><span data-stu-id="3d43c-107">Specify the path of a .mof file.</span></span>

## <span data-ttu-id="3d43c-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3d43c-108">EXAMPLES</span></span>

### <span data-ttu-id="3d43c-109">Пример 1. Импорт конфигурации узла DSC в автоматизацию</span><span class="sxs-lookup"><span data-stu-id="3d43c-109">Example 1: Import a DSC node configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -Force
```

<span data-ttu-id="3d43c-110">Эта команда импортирует конфигурацию узла DSC из файла webserver.mof в учетную запись автоматизации Contoso17 в конфигурации DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d43c-110">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="3d43c-111">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="3d43c-111">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3d43c-112">Если имеется существующая конфигурация узла DSC с именем ContosoConfiguration.webserver, эта команда заменяет ее.</span><span class="sxs-lookup"><span data-stu-id="3d43c-112">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command replaces it.</span></span>

### <span data-ttu-id="3d43c-113">Пример 2. Импорт конфигурации узла DSC в автоматизацию и создание новой версии сборки без переописи существующей настройки NodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d43c-113">Example 2: Import a DSC node configuration into Automation and create a new build version and not overwrite existing NodeConfiguration.</span></span>
```
PS C:\>Import-AzAutomationDscNodeConfiguration -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ConfigurationName "ContosoConfiguration" -Path "C:\DSC\webserver.mof" -IncrementNodeConfigurationBuild
```

<span data-ttu-id="3d43c-114">Эта команда импортирует конфигурацию узла DSC из файла webserver.mof в учетную запись автоматизации Contoso17 в конфигурации DSC ContosoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d43c-114">This command imports a DSC node configuration from the file named webserver.mof into the Automation account named Contoso17, under the DSC configuration ContosoConfiguration.</span></span>
<span data-ttu-id="3d43c-115">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="3d43c-115">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3d43c-116">Если существует существующая конфигурация узла DSC с именем ContosoConfiguration.webserver, эта команда добавляет новую версию сборки с именем ContosoConfiguration[2].webserver.</span><span class="sxs-lookup"><span data-stu-id="3d43c-116">If there is an existing DSC node configuration named ContosoConfiguration.webserver, this command adds a new build version with the name ContosoConfiguration[2].webserver.</span></span>

## <span data-ttu-id="3d43c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d43c-117">PARAMETERS</span></span>

### <span data-ttu-id="3d43c-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3d43c-118">-AutomationAccountName</span></span>
<span data-ttu-id="3d43c-119">Указывает имя учетной записи автоматизации, в которую этот cmdlet импортирует конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="3d43c-119">Specifies the name of the Automation account into which this cmdlet imports a DSC node configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d43c-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="3d43c-120">-ConfigurationName</span></span>
<span data-ttu-id="3d43c-121">Имя конфигурации DSC в автоматизации, которая будет использовать в качестве пространства имен и контейнера для импорта конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="3d43c-121">Specifies the name of a DSC configuration in Automation to use as the namespace and container for the node configuration to import.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d43c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d43c-122">-DefaultProfile</span></span>
<span data-ttu-id="3d43c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3d43c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3d43c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="3d43c-124">-Force</span></span>
<span data-ttu-id="3d43c-125">Указывает на то, что этот cmdlet заменяет существующую конфигурацию узла DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="3d43c-125">Indicates that this cmdlet replaces an existing DSC node configuration in Automation.</span></span>

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

### <span data-ttu-id="3d43c-126">-IncrementNodeConfigurationBuild</span><span class="sxs-lookup"><span data-stu-id="3d43c-126">-IncrementNodeConfigurationBuild</span></span>
<span data-ttu-id="3d43c-127">Создает новую версию сборки конфигурации узла.</span><span class="sxs-lookup"><span data-stu-id="3d43c-127">Creates a new Node Configuration build version.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d43c-128">-Path</span><span class="sxs-lookup"><span data-stu-id="3d43c-128">-Path</span></span>
<span data-ttu-id="3d43c-129">Путь к документу конфигурации "КУФ", который импортируется этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d43c-129">Specifies the path of the MOF configuration document that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d43c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d43c-130">-ResourceGroupName</span></span>
<span data-ttu-id="3d43c-131">Имя группы ресурсов, для которой этот cmdlet импортирует конфигурацию узла DSC.</span><span class="sxs-lookup"><span data-stu-id="3d43c-131">Specifies the name of a resource group for which this cmdlet imports a DSC node configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d43c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d43c-132">-Confirm</span></span>
<span data-ttu-id="3d43c-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d43c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d43c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d43c-134">-WhatIf</span></span>
<span data-ttu-id="3d43c-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d43c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d43c-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3d43c-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d43c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d43c-137">CommonParameters</span></span>
<span data-ttu-id="3d43c-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d43c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d43c-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d43c-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d43c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3d43c-140">INPUTS</span></span>

### <span data-ttu-id="3d43c-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3d43c-141">System.String</span></span>

## <span data-ttu-id="3d43c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3d43c-142">OUTPUTS</span></span>

### <span data-ttu-id="3d43c-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d43c-143">Microsoft.Azure.Commands.Automation.Model.NodeConfiguration</span></span>

## <span data-ttu-id="3d43c-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3d43c-144">NOTES</span></span>

## <span data-ttu-id="3d43c-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3d43c-145">RELATED LINKS</span></span>

[<span data-ttu-id="3d43c-146">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d43c-146">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="3d43c-147">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="3d43c-147">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)



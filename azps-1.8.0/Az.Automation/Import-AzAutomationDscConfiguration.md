---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/import-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Import-AzAutomationDscConfiguration.md
ms.openlocfilehash: e1e7ed85a43492f4e00495df52f51c49712c4aff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731583"
---
# <span data-ttu-id="f1516-101">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1516-101">Import-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="f1516-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f1516-102">SYNOPSIS</span></span>
<span data-ttu-id="f1516-103">Импортирует конфигурацию DSC в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="f1516-103">Imports a DSC configuration into Automation.</span></span>

## <span data-ttu-id="f1516-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f1516-104">SYNTAX</span></span>

```
Import-AzAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1516-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1516-105">DESCRIPTION</span></span>
<span data-ttu-id="f1516-106">Командлет **Import-AzAutomationDscConfiguration** импортирует конфигурацию необходимой конфигурации (DSC) ТД в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f1516-106">The **Import-AzAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="f1516-107">Укажите путь к сценарию AP, содержащему единственную конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="f1516-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="f1516-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f1516-108">EXAMPLES</span></span>

### <span data-ttu-id="f1516-109">Пример 1: импорт конфигурации DSC в автоматизацию</span><span class="sxs-lookup"><span data-stu-id="f1516-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="f1516-110">Эта команда импортирует конфигурацию DSC в файле с именем client.ps1 в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f1516-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="f1516-111">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="f1516-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="f1516-112">Если у вас уже есть конфигурация DSC, эта команда заменяет ее.</span><span class="sxs-lookup"><span data-stu-id="f1516-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="f1516-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f1516-113">PARAMETERS</span></span>

### <span data-ttu-id="f1516-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f1516-114">-AutomationAccountName</span></span>
<span data-ttu-id="f1516-115">Указывает имя учетной записи автоматизации, на которую этот командлет импортирует конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="f1516-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="f1516-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1516-116">-DefaultProfile</span></span>
<span data-ttu-id="f1516-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f1516-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f1516-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="f1516-118">-Description</span></span>
<span data-ttu-id="f1516-119">Задает описание конфигурации, импортируемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f1516-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1516-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f1516-120">-Force</span></span>
<span data-ttu-id="f1516-121">Указывает на то, что этот командлет заменяет существующую конфигурацию DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f1516-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

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

### <span data-ttu-id="f1516-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="f1516-122">-LogVerbose</span></span>
<span data-ttu-id="f1516-123">Указывает, включает ли этот командлет подробный вход и отключение для заданий компиляции данной конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="f1516-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="f1516-124">Укажите значение $True, чтобы включить или отключить подробный вход, и $False, чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="f1516-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1516-125">-Опубликовано</span><span class="sxs-lookup"><span data-stu-id="f1516-125">-Published</span></span>
<span data-ttu-id="f1516-126">Указывает на то, что этот командлет импортирует конфигурацию DSC в опубликованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="f1516-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

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

### <span data-ttu-id="f1516-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1516-127">-ResourceGroupName</span></span>
<span data-ttu-id="f1516-128">Указывает имя группы ресурсов, для которой этот командлет импортирует конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="f1516-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

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

### <span data-ttu-id="f1516-129">-Источник</span><span class="sxs-lookup"><span data-stu-id="f1516-129">-SourcePath</span></span>
<span data-ttu-id="f1516-130">Указывает путь wps_2 сценария, содержащего конфигурацию DSC, которую этот командлет импортирует.</span><span class="sxs-lookup"><span data-stu-id="f1516-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1516-131">-Теги</span><span class="sxs-lookup"><span data-stu-id="f1516-131">-Tags</span></span>
<span data-ttu-id="f1516-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="f1516-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f1516-133">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="f1516-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1516-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f1516-134">-Confirm</span></span>
<span data-ttu-id="f1516-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f1516-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1516-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1516-136">-WhatIf</span></span>
<span data-ttu-id="f1516-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f1516-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1516-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f1516-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1516-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1516-139">CommonParameters</span></span>
<span data-ttu-id="f1516-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f1516-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1516-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1516-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1516-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f1516-142">INPUTS</span></span>

### <span data-ttu-id="f1516-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f1516-143">System.String</span></span>

### <span data-ttu-id="f1516-144">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="f1516-144">System.Collections.IDictionary</span></span>

### <span data-ttu-id="f1516-145">System. Nullable "1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f1516-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f1516-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f1516-146">OUTPUTS</span></span>

### <span data-ttu-id="f1516-147">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1516-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="f1516-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="f1516-148">NOTES</span></span>

## <span data-ttu-id="f1516-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f1516-149">RELATED LINKS</span></span>

[<span data-ttu-id="f1516-150">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1516-150">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="f1516-151">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1516-151">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

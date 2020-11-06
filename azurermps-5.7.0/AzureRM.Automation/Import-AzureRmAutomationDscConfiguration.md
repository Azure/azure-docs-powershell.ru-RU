---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BA508F0B-847F-4531-9D5D-A5A044A2D207
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/import-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Import-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: e8d7cfcf595d7dd445d66865d922676c96b7e6d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557607"
---
# <span data-ttu-id="a73cf-101">Import-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a73cf-101">Import-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="a73cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a73cf-102">SYNOPSIS</span></span>
<span data-ttu-id="a73cf-103">Импортирует конфигурацию DSC в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="a73cf-103">Imports a DSC configuration into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a73cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a73cf-104">SYNTAX</span></span>

```
Import-AzureRmAutomationDscConfiguration -SourcePath <String> [-Tags <IDictionary>] [-Description <String>]
 [-Published] [-Force] [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a73cf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a73cf-105">DESCRIPTION</span></span>
<span data-ttu-id="a73cf-106">Командлет **Import-AzureRmAutomationDscConfiguration** импортирует конфигурацию необходимой конфигурации (DSC) ТД в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a73cf-106">The **Import-AzureRmAutomationDscConfiguration** cmdlet imports an APS Desired State Configuration (DSC) configuration into Azure Automation.</span></span>
<span data-ttu-id="a73cf-107">Укажите путь к сценарию AP, содержащему единственную конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="a73cf-107">Specify the path of an APS script that contains a single DSC configuration.</span></span>

## <span data-ttu-id="a73cf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a73cf-108">EXAMPLES</span></span>

### <span data-ttu-id="a73cf-109">Пример 1: импорт конфигурации DSC в автоматизацию</span><span class="sxs-lookup"><span data-stu-id="a73cf-109">Example 1: Import a DSC configuration into Automation</span></span>
```
PS C:\>Import-AzureRmAutomationDscConfiguration -AutomationAccountName "Contoso17"-ResourceGroupName "ResourceGroup01" -SourcePath "C:\DSC\client.ps1" -Force
```

<span data-ttu-id="a73cf-110">Эта команда импортирует конфигурацию DSC в файле с именем client.ps1 в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a73cf-110">This command imports the DSC configuration in the file named client.ps1 into the Automation account named Contoso17.</span></span> <span data-ttu-id="a73cf-111">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="a73cf-111">The command specifies the *Force* parameter.</span></span> <span data-ttu-id="a73cf-112">Если у вас уже есть конфигурация DSC, эта команда заменяет ее.</span><span class="sxs-lookup"><span data-stu-id="a73cf-112">If there is an existing DSC configuration, this command replaces it.</span></span>

## <span data-ttu-id="a73cf-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a73cf-113">PARAMETERS</span></span>

### <span data-ttu-id="a73cf-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a73cf-114">-AutomationAccountName</span></span>
<span data-ttu-id="a73cf-115">Указывает имя учетной записи автоматизации, на которую этот командлет импортирует конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="a73cf-115">Specifies the name of the Automation account into which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73cf-116">-DefaultProfile</span></span>
<span data-ttu-id="a73cf-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a73cf-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-118">-Описание</span><span class="sxs-lookup"><span data-stu-id="a73cf-118">-Description</span></span>
<span data-ttu-id="a73cf-119">Задает описание конфигурации, импортируемой этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a73cf-119">Specifies a description of the configuration that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a73cf-120">-Force</span></span>
<span data-ttu-id="a73cf-121">Указывает на то, что этот командлет заменяет существующую конфигурацию DSC в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="a73cf-121">Indicates that this cmdlet replaces an existing DSC configuration in Automation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-122">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="a73cf-122">-LogVerbose</span></span>
<span data-ttu-id="a73cf-123">Указывает, включает ли этот командлет подробный вход и отключение для заданий компиляции данной конфигурации DSC.</span><span class="sxs-lookup"><span data-stu-id="a73cf-123">Specifies whether this cmdlet turns verbose logging on or off for compilation jobs of this DSC configuration.</span></span> <span data-ttu-id="a73cf-124">Укажите значение $True, чтобы включить или отключить подробный вход, и $False, чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="a73cf-124">Specify a value of $True to turn verbose logging on or $False to turn it off.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-125">-Опубликовано</span><span class="sxs-lookup"><span data-stu-id="a73cf-125">-Published</span></span>
<span data-ttu-id="a73cf-126">Указывает на то, что этот командлет импортирует конфигурацию DSC в опубликованном состоянии.</span><span class="sxs-lookup"><span data-stu-id="a73cf-126">Indicates that this cmdlet imports the DSC configuration in the published state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="a73cf-128">Указывает имя группы ресурсов, для которой этот командлет импортирует конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="a73cf-128">Specifies the name of a resource group for which this cmdlet imports a DSC configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-129">-Источник</span><span class="sxs-lookup"><span data-stu-id="a73cf-129">-SourcePath</span></span>
<span data-ttu-id="a73cf-130">Указывает путь wps_2 сценария, содержащего конфигурацию DSC, которую этот командлет импортирует.</span><span class="sxs-lookup"><span data-stu-id="a73cf-130">Specifies the path of the wps_2 script that contains the DSC configuration that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-131">-Теги</span><span class="sxs-lookup"><span data-stu-id="a73cf-131">-Tags</span></span>
<span data-ttu-id="a73cf-132">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a73cf-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a73cf-133">Например:</span><span class="sxs-lookup"><span data-stu-id="a73cf-133">For example:</span></span>

<span data-ttu-id="a73cf-134">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="a73cf-134">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a73cf-135">-Confirm</span></span>
<span data-ttu-id="a73cf-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a73cf-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a73cf-137">-WhatIf</span></span>
<span data-ttu-id="a73cf-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a73cf-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a73cf-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a73cf-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73cf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73cf-140">CommonParameters</span></span>
<span data-ttu-id="a73cf-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a73cf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73cf-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a73cf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73cf-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a73cf-143">INPUTS</span></span>

### <span data-ttu-id="a73cf-144">Ничего</span><span class="sxs-lookup"><span data-stu-id="a73cf-144">None</span></span>
<span data-ttu-id="a73cf-145">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="a73cf-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a73cf-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a73cf-146">OUTPUTS</span></span>

### <span data-ttu-id="a73cf-147">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a73cf-147">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="a73cf-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="a73cf-148">NOTES</span></span>

## <span data-ttu-id="a73cf-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a73cf-149">RELATED LINKS</span></span>

[<span data-ttu-id="a73cf-150">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a73cf-150">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="a73cf-151">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="a73cf-151">Get-AzureRmAutomationDscConfiguration</span></span>](./Get-AzureRmAutomationDscConfiguration.md)

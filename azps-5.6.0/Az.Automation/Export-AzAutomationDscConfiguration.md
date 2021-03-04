---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 595D3304-3331-4F44-BA57-AE090FB8A132
online version: https://docs.microsoft.com/powershell/module/az.automation/export-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Export-AzAutomationDscConfiguration.md
ms.openlocfilehash: c27f878d2dbb0e52a16216a2158c737bc523c932
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959032"
---
# <span data-ttu-id="56973-101">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="56973-101">Export-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="56973-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56973-102">SYNOPSIS</span></span>
<span data-ttu-id="56973-103">Экспорт конфигурации DSC из автоматизации в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="56973-103">Exports a DSC configuration from Automation to a local file.</span></span>

## <span data-ttu-id="56973-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56973-104">SYNTAX</span></span>

```
Export-AzAutomationDscConfiguration -Name <String> [-Slot <String>] [-OutputFolder <String>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56973-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56973-105">DESCRIPTION</span></span>
<span data-ttu-id="56973-106">Для **экспорта-AzAutomationDscConfiguration** экспортируется конфигурация APS Desired State Configuration (DSC) из Azure Automation в локальный файл.</span><span class="sxs-lookup"><span data-stu-id="56973-106">The **Export-AzAutomationDscConfiguration** cmdlet exports an APS Desired State Configuration (DSC) configuration from Azure Automation to a local file.</span></span>
<span data-ttu-id="56973-107">Файл экспортируется с расширением PS1.</span><span class="sxs-lookup"><span data-stu-id="56973-107">The exported file has a .ps1 file name extension.</span></span>

## <span data-ttu-id="56973-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56973-108">EXAMPLES</span></span>

### <span data-ttu-id="56973-109">Пример 1. Экспорт опубликованной версии конфигурации DSC</span><span class="sxs-lookup"><span data-stu-id="56973-109">Example 1: Export the published version of a DSC configuration</span></span>
```
PS C:\>Export-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup01" -AutomationAccountName "AutomationAccount01" -Name "Configuration01" -Slot Published -OutputFolder "C:\Users\PattiFuller\Desktop"
```

<span data-ttu-id="56973-110">Эта команда экспортирует опубликованную версию конфигурации DSC в автоматизацию в указанную папку на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="56973-110">This command exports the published version of a DSC configuration in Automation to the specified folder, which is the desktop.</span></span>

## <span data-ttu-id="56973-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56973-111">PARAMETERS</span></span>

### <span data-ttu-id="56973-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="56973-112">-AutomationAccountName</span></span>
<span data-ttu-id="56973-113">Указывает имя учетной записи автоматизации, которая содержит DSC, экспортируемую этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56973-113">Specifies the name of the Automation account that contains the DSC that this cmdlet exports.</span></span>

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

### <span data-ttu-id="56973-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56973-114">-DefaultProfile</span></span>
<span data-ttu-id="56973-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="56973-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56973-116">-Force</span><span class="sxs-lookup"><span data-stu-id="56973-116">-Force</span></span>
<span data-ttu-id="56973-117">Указывает на то, что этот cmdlet заменяет существующий локальный файл новым файлом с таким же именем.</span><span class="sxs-lookup"><span data-stu-id="56973-117">Indicates that this cmdlet replaces an existing local file with a new file that has the same name.</span></span>

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

### <span data-ttu-id="56973-118">-Name</span><span class="sxs-lookup"><span data-stu-id="56973-118">-Name</span></span>
<span data-ttu-id="56973-119">Указывает имя конфигурации DSC, экспортируемой этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56973-119">Specifies the name of the DSC configuration that this cmdlet exports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56973-120">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="56973-120">-OutputFolder</span></span>
<span data-ttu-id="56973-121">Определяет папку вывода, в которой этот cmdlet экспортирует конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="56973-121">Specifies the output folder where this cmdlet exports the DSC configuration.</span></span>

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

### <span data-ttu-id="56973-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56973-122">-ResourceGroupName</span></span>
<span data-ttu-id="56973-123">Имя группы ресурсов, для которой этот cmdlet экспортирует конфигурацию DSC.</span><span class="sxs-lookup"><span data-stu-id="56973-123">Specifies the name of a resource group for which this cmdlet exports a DSC configuration.</span></span>

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

### <span data-ttu-id="56973-124">-Slot</span><span class="sxs-lookup"><span data-stu-id="56973-124">-Slot</span></span>
<span data-ttu-id="56973-125">Определяет версию конфигурации DSC, экспортируемую этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56973-125">Specifies which version of the DSC configuration that this cmdlet exports.</span></span>
<span data-ttu-id="56973-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="56973-126">Valid values are:</span></span> 
- <span data-ttu-id="56973-127">Черновик</span><span class="sxs-lookup"><span data-stu-id="56973-127">Draft</span></span>
- <span data-ttu-id="56973-128">Опубликовано значение по умолчанию "Опубликовано".</span><span class="sxs-lookup"><span data-stu-id="56973-128">Published The default value is Published.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Published, Draft

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56973-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56973-129">-Confirm</span></span>
<span data-ttu-id="56973-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56973-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56973-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56973-131">-WhatIf</span></span>
<span data-ttu-id="56973-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56973-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56973-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="56973-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56973-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56973-134">CommonParameters</span></span>
<span data-ttu-id="56973-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56973-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56973-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56973-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56973-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56973-137">INPUTS</span></span>

### <span data-ttu-id="56973-138">System.String</span><span class="sxs-lookup"><span data-stu-id="56973-138">System.String</span></span>

## <span data-ttu-id="56973-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56973-139">OUTPUTS</span></span>

### <span data-ttu-id="56973-140">System.IO.DirectoryInfo</span><span class="sxs-lookup"><span data-stu-id="56973-140">System.IO.DirectoryInfo</span></span>

## <span data-ttu-id="56973-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56973-141">NOTES</span></span>

## <span data-ttu-id="56973-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56973-142">RELATED LINKS</span></span>

[<span data-ttu-id="56973-143">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="56973-143">Get-AzAutomationDscConfiguration</span></span>](./Get-AzAutomationDscConfiguration.md)

[<span data-ttu-id="56973-144">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="56973-144">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)



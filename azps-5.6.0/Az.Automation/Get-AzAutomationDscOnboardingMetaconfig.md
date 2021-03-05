---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: e520fec3d0299ca2b5f74bb2a8a8b7de437d7a2a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008152"
---
# <span data-ttu-id="aaf68-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="aaf68-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="aaf68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaf68-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf68-103">Создает MOF-файлы с мета конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="aaf68-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="aaf68-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aaf68-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaf68-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aaf68-105">DESCRIPTION</span></span>
<span data-ttu-id="aaf68-106">С помощью cmdlet **get-AzAutomationDscOnboardingMetaconfig** создается файл APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="aaf68-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="aaf68-107">Этот cmdlet creates a MOF file for each computer name that you specify.</span><span class="sxs-lookup"><span data-stu-id="aaf68-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="aaf68-108">Для MOF-файлов будет создаваться папка.</span><span class="sxs-lookup"><span data-stu-id="aaf68-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="aaf68-109">Вы можете выполнить Set-DscLocalConfigurationManager этой папки, чтобы эти компьютеры были в учетной записи автоматизации Azure как узлы DSC.</span><span class="sxs-lookup"><span data-stu-id="aaf68-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="aaf68-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aaf68-110">EXAMPLES</span></span>

### <span data-ttu-id="aaf68-111">Пример 1. Серверы в сфере автоматизации DSC</span><span class="sxs-lookup"><span data-stu-id="aaf68-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="aaf68-112">Первая команда создает файлы мета конфигурации DSC для двух серверов для учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="aaf68-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="aaf68-113">Эта команда сохраняет эти файлы на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="aaf68-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="aaf68-114">Вторая команда использует командлет **Set-DscLocalConfigurationManager** для применения метаконфигуры к указанным компьютерам для их переноса в качестве узлов DSC.</span><span class="sxs-lookup"><span data-stu-id="aaf68-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="aaf68-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaf68-115">PARAMETERS</span></span>

### <span data-ttu-id="aaf68-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="aaf68-116">-AutomationAccountName</span></span>
<span data-ttu-id="aaf68-117">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="aaf68-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="aaf68-118">Вы можете войдировать компьютеры, которые указывает *параметр ComputerName,* в учетную запись, указанную этим параметром.</span><span class="sxs-lookup"><span data-stu-id="aaf68-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="aaf68-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="aaf68-119">-ComputerName</span></span>
<span data-ttu-id="aaf68-120">Определяет массив имен компьютеров, для которых этот cmdlet создает MOF-файлы.</span><span class="sxs-lookup"><span data-stu-id="aaf68-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="aaf68-121">Если этот параметр не задан, с помощью cmdlet создается MOF-файл для текущего компьютера (localhost).</span><span class="sxs-lookup"><span data-stu-id="aaf68-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aaf68-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf68-122">-DefaultProfile</span></span>
<span data-ttu-id="aaf68-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aaf68-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aaf68-124">-Force</span><span class="sxs-lookup"><span data-stu-id="aaf68-124">-Force</span></span>
<span data-ttu-id="aaf68-125">Запуск команды без запроса на подтверждение и замену MOF-файлов с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="aaf68-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="aaf68-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="aaf68-126">-OutputFolder</span></span>
<span data-ttu-id="aaf68-127">Указывает имя папки, в которой этот cmdlet хранит MOF-файлы.</span><span class="sxs-lookup"><span data-stu-id="aaf68-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="aaf68-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf68-128">-ResourceGroupName</span></span>
<span data-ttu-id="aaf68-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aaf68-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="aaf68-130">Этот cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span><span class="sxs-lookup"><span data-stu-id="aaf68-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="aaf68-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaf68-131">-Confirm</span></span>
<span data-ttu-id="aaf68-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaf68-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaf68-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf68-133">-WhatIf</span></span>
<span data-ttu-id="aaf68-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aaf68-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaf68-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aaf68-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaf68-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf68-136">CommonParameters</span></span>
<span data-ttu-id="aaf68-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaf68-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf68-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaf68-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf68-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aaf68-139">INPUTS</span></span>

### <span data-ttu-id="aaf68-140">System.String</span><span class="sxs-lookup"><span data-stu-id="aaf68-140">System.String</span></span>

### <span data-ttu-id="aaf68-141">System.String[]</span><span class="sxs-lookup"><span data-stu-id="aaf68-141">System.String[]</span></span>

## <span data-ttu-id="aaf68-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aaf68-142">OUTPUTS</span></span>

### <span data-ttu-id="aaf68-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="aaf68-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="aaf68-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aaf68-144">NOTES</span></span>

## <span data-ttu-id="aaf68-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aaf68-145">RELATED LINKS</span></span>

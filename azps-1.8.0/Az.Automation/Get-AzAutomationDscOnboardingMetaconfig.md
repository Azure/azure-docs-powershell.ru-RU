---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: FB331566-AC13-4751-A600-3A0E576308C7
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsconboardingmetaconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscOnboardingMetaconfig.md
ms.openlocfilehash: 0302803568bac71baed28615552848f113da32df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731620"
---
# <span data-ttu-id="5634e-101">Get-AzAutomationDscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="5634e-101">Get-AzAutomationDscOnboardingMetaconfig</span></span>

## <span data-ttu-id="5634e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5634e-102">SYNOPSIS</span></span>
<span data-ttu-id="5634e-103">Создает MOF-файлы с метаконфигурации.</span><span class="sxs-lookup"><span data-stu-id="5634e-103">Creates meta-configuration .mof files.</span></span>

## <span data-ttu-id="5634e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5634e-104">SYNTAX</span></span>

```
Get-AzAutomationDscOnboardingMetaconfig [-OutputFolder <String>] [-ComputerName <String[]>] [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5634e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5634e-105">DESCRIPTION</span></span>
<span data-ttu-id="5634e-106">Командлет **Get-AzAutomationDscOnboardingMetaconfig** создает протоколы MOF-файлов, которые нужно использовать в МЕТАКОНФИГУРАЦИИ (DSC).</span><span class="sxs-lookup"><span data-stu-id="5634e-106">The **Get-AzAutomationDscOnboardingMetaconfig** cmdlet creates APS Desired State Configuration (DSC) meta-configuration Managed Object Format (MOF) files.</span></span>
<span data-ttu-id="5634e-107">Этот командлет создает MOF-файл для каждого указываемого имени компьютера.</span><span class="sxs-lookup"><span data-stu-id="5634e-107">This cmdlet creates a .mof file for each computer name that you specify.</span></span>
<span data-ttu-id="5634e-108">Командлет создает папку для файлов. mof.</span><span class="sxs-lookup"><span data-stu-id="5634e-108">The cmdlet creates a folder for the .mof files.</span></span>
<span data-ttu-id="5634e-109">Вы можете выполнить командлет Set-DscLocalConfigurationManager для этой папки, чтобы присоединить эти компьютеры к учетной записи службы автоматизации Azure как узлы DSC.</span><span class="sxs-lookup"><span data-stu-id="5634e-109">You can run the Set-DscLocalConfigurationManager cmdlet for this folder to onboard these computers into an Azure Automation account as DSC nodes.</span></span>

## <span data-ttu-id="5634e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5634e-110">EXAMPLES</span></span>

### <span data-ttu-id="5634e-111">Пример 1: Встроенные серверы в автоматизацию DSC</span><span class="sxs-lookup"><span data-stu-id="5634e-111">Example 1: Onboard servers to Automation DSC</span></span>
```
PS C:\>Get-AzAutomationDscOnboardingMetaconfig -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ComputerName "Server01", "Server02" -OutputFolder "C:\Users\PattiFuller\Desktop" 
PS C:\> Set-DscLocalConfigurationManager -Path "C:\Users\PattiFuller\Desktop\DscMetaConfigs" -ComputerName "Server01", "Server02"
```

<span data-ttu-id="5634e-112">Первая команда создает файлы мета-конфигурации DSC для двух серверов для учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5634e-112">The first command creates DSC meta-configuration files for two servers for the Automation account named Contoso17.</span></span>
<span data-ttu-id="5634e-113">Команда сохраняет эти файлы на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="5634e-113">The command saves these files on a desktop.</span></span>
<span data-ttu-id="5634e-114">Вторая команда использует командлет **Set-DscLocalConfigurationManager** , чтобы применить мета-конфигурацию к указанным компьютерам для их пошагового использования в качестве узлов DSC.</span><span class="sxs-lookup"><span data-stu-id="5634e-114">The second command uses the **Set-DscLocalConfigurationManager** cmdlet to apply the meta-configuration to the specified computers to onboard them as DSC nodes.</span></span>

## <span data-ttu-id="5634e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5634e-115">PARAMETERS</span></span>

### <span data-ttu-id="5634e-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5634e-116">-AutomationAccountName</span></span>
<span data-ttu-id="5634e-117">Указывает имя учетной записи автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5634e-117">Specifies the name of an Automation account.</span></span>
<span data-ttu-id="5634e-118">Вы можете выплата компьютеров, параметр *ComputerName* которых указывает на учетную запись, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="5634e-118">You can onboard the computers that the *ComputerName* parameter specifies to the account that this parameter specifies.</span></span>

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

### <span data-ttu-id="5634e-119">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="5634e-119">-ComputerName</span></span>
<span data-ttu-id="5634e-120">Указывает массив имен компьютеров, для которых этот командлет создает MOF-файлы.</span><span class="sxs-lookup"><span data-stu-id="5634e-120">Specifies an array of names of computers for which this cmdlet generates .mof files.</span></span>
<span data-ttu-id="5634e-121">Если этот параметр не указан, командлет создает MOF-файл для текущего компьютера (localhost).</span><span class="sxs-lookup"><span data-stu-id="5634e-121">If you do not specify this parameter, the cmdlet generates an .mof file for the current computer (localhost).</span></span>

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

### <span data-ttu-id="5634e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5634e-122">-DefaultProfile</span></span>
<span data-ttu-id="5634e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5634e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5634e-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5634e-124">-Force</span></span>
<span data-ttu-id="5634e-125">Принудительное выполнение команды без запроса подтверждения и замена существующих MOF-файлов с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="5634e-125">Forces the command to run without prompting you for confirmation, and to replace existing .mof files that have the same name.</span></span>

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

### <span data-ttu-id="5634e-126">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="5634e-126">-OutputFolder</span></span>
<span data-ttu-id="5634e-127">Указывает имя папки, в которой этот командлет хранит MOF-файлы.</span><span class="sxs-lookup"><span data-stu-id="5634e-127">Specifies the name of a folder where this cmdlet stores .mof files.</span></span>

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

### <span data-ttu-id="5634e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5634e-128">-ResourceGroupName</span></span>
<span data-ttu-id="5634e-129">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5634e-129">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5634e-130">Этот командлет создает файлы. mof на интегрированных компьютерах в группе ресурсов, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="5634e-130">This cmdlet creates .mof files to onboard computers in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5634e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5634e-131">-Confirm</span></span>
<span data-ttu-id="5634e-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5634e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5634e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5634e-133">-WhatIf</span></span>
<span data-ttu-id="5634e-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5634e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5634e-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5634e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5634e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5634e-136">CommonParameters</span></span>
<span data-ttu-id="5634e-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5634e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5634e-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5634e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5634e-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5634e-139">INPUTS</span></span>

### <span data-ttu-id="5634e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5634e-140">System.String</span></span>

### <span data-ttu-id="5634e-141">System. String []</span><span class="sxs-lookup"><span data-stu-id="5634e-141">System.String[]</span></span>

## <span data-ttu-id="5634e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5634e-142">OUTPUTS</span></span>

### <span data-ttu-id="5634e-143">Microsoft. Azure. Commands. Automation. Model. DscOnboardingMetaconfig</span><span class="sxs-lookup"><span data-stu-id="5634e-143">Microsoft.Azure.Commands.Automation.Model.DscOnboardingMetaconfig</span></span>

## <span data-ttu-id="5634e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5634e-144">NOTES</span></span>

## <span data-ttu-id="5634e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5634e-145">RELATED LINKS</span></span>

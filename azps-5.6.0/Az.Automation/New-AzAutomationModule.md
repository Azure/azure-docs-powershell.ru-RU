---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 093a6f61668f40b43d2f228035132c010e31d426
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012728"
---
# <span data-ttu-id="bcf90-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="bcf90-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="bcf90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bcf90-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf90-103">Импорт модуля в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="bcf90-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="bcf90-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bcf90-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcf90-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcf90-105">DESCRIPTION</span></span>
<span data-ttu-id="bcf90-106">Командлет **New-AzAutomationModule** импортирует модуль в автоматизацию Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf90-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="bcf90-107">Эта команда принимает сжатый файл с расширением ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="bcf90-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="bcf90-108">Файл содержит папку, включаемую файл одного из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="bcf90-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="bcf90-109">Windows PowerShell, который имеет расширение PSM1 или DLL</span><span class="sxs-lookup"><span data-stu-id="bcf90-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="bcf90-110">Windows PowerShell модуль с расширением PSD1: имя ZIP-файла, имя папки и имя файла в папке должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="bcf90-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="bcf90-111">Укажите ZIP-файл как URL-адрес, доступный службе автоматизации.</span><span class="sxs-lookup"><span data-stu-id="bcf90-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="bcf90-112">При импорте Windows PowerShell модуля в автоматизацию с помощью этого командлета или Set-AzAutomationModule командлета операция является асинхронной.</span><span class="sxs-lookup"><span data-stu-id="bcf90-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="bcf90-113">Команда завершает процесс в зависимости от успешного или неудачного завершения импорта.</span><span class="sxs-lookup"><span data-stu-id="bcf90-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="bcf90-114">Чтобы проверить успешности, запустите следующую команду: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName Проверьте свойство **ProvisioningState** на значение "Успешно".</span><span class="sxs-lookup"><span data-stu-id="bcf90-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="bcf90-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bcf90-115">EXAMPLES</span></span>

### <span data-ttu-id="bcf90-116">Пример 1. Импорт модуля</span><span class="sxs-lookup"><span data-stu-id="bcf90-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="bcf90-117">Эта команда импортирует модуль ContosoModule в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="bcf90-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="bcf90-118">Модуль хранится в BLOB-проекте Azure в учетной записи хранения contosostorage и контейнере с именами модулей.</span><span class="sxs-lookup"><span data-stu-id="bcf90-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="bcf90-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bcf90-119">PARAMETERS</span></span>

### <span data-ttu-id="bcf90-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bcf90-120">-AutomationAccountName</span></span>
<span data-ttu-id="bcf90-121">Указывает имя учетной записи автоматизации, для которой этот командлет импортирует модуль.</span><span class="sxs-lookup"><span data-stu-id="bcf90-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="bcf90-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="bcf90-122">-ContentLinkUri</span></span>
<span data-ttu-id="bcf90-123">URL-адрес zip-пакета модуля</span><span class="sxs-lookup"><span data-stu-id="bcf90-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf90-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf90-124">-DefaultProfile</span></span>
<span data-ttu-id="bcf90-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bcf90-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bcf90-126">-Name</span><span class="sxs-lookup"><span data-stu-id="bcf90-126">-Name</span></span>
<span data-ttu-id="bcf90-127">Указывает имя модуля, который импортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="bcf90-127">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcf90-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf90-128">-ResourceGroupName</span></span>
<span data-ttu-id="bcf90-129">Имя группы ресурсов, для которой этот командлет импортирует модуль.</span><span class="sxs-lookup"><span data-stu-id="bcf90-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="bcf90-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf90-130">CommonParameters</span></span>
<span data-ttu-id="bcf90-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf90-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcf90-132">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf90-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf90-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bcf90-133">INPUTS</span></span>

### <span data-ttu-id="bcf90-134">System.String</span><span class="sxs-lookup"><span data-stu-id="bcf90-134">System.String</span></span>

### <span data-ttu-id="bcf90-135">System.Uri</span><span class="sxs-lookup"><span data-stu-id="bcf90-135">System.Uri</span></span>

## <span data-ttu-id="bcf90-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bcf90-136">OUTPUTS</span></span>

### <span data-ttu-id="bcf90-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="bcf90-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="bcf90-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bcf90-138">NOTES</span></span>

## <span data-ttu-id="bcf90-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcf90-139">RELATED LINKS</span></span>

[<span data-ttu-id="bcf90-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="bcf90-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="bcf90-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="bcf90-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="bcf90-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="bcf90-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)



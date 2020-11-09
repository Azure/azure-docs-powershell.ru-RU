---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315308"
---
# <span data-ttu-id="9ed90-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9ed90-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="9ed90-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ed90-102">SYNOPSIS</span></span>
<span data-ttu-id="9ed90-103">Импортирует модуль в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="9ed90-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="9ed90-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ed90-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ed90-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ed90-105">DESCRIPTION</span></span>
<span data-ttu-id="9ed90-106">Командлет **New-AzAutomationModule** импортирует модуль в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="9ed90-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="9ed90-107">Эта команда принимает сжатый файл с расширением ZIP.</span><span class="sxs-lookup"><span data-stu-id="9ed90-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="9ed90-108">Файл содержит папку, в которую входит файл одного из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="9ed90-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="9ed90-109">Модуль Windows PowerShell, имеющий расширение имени файла. PSM1 или. dll</span><span class="sxs-lookup"><span data-stu-id="9ed90-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="9ed90-110">Манифест модуля Windows PowerShell, имеющий расширение имени файла. PSD1, имя ZIP-файла, имя папки, а также имя файла в папке должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="9ed90-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="9ed90-111">Укажите ZIP-файл, который может получать Access служба автоматизации.</span><span class="sxs-lookup"><span data-stu-id="9ed90-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="9ed90-112">При импорте модуля Windows PowerShell в автоматизацию с помощью этого командлета или командлета Set-AzAutomationModule операция асинхронна.</span><span class="sxs-lookup"><span data-stu-id="9ed90-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="9ed90-113">Команда завершает выполнение импорта или завершается неуспешно.</span><span class="sxs-lookup"><span data-stu-id="9ed90-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="9ed90-114">Чтобы проверить, успешно ли она выполнена, выполните следующую команду: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName убедитесь, что свойство **ProvisioningState** для значения SUCCEEDED.</span><span class="sxs-lookup"><span data-stu-id="9ed90-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="9ed90-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ed90-115">EXAMPLES</span></span>

### <span data-ttu-id="9ed90-116">Пример 1: импорт модуля</span><span class="sxs-lookup"><span data-stu-id="9ed90-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9ed90-117">Эта команда импортирует модуль с именем ContosoModule в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="9ed90-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="9ed90-118">Модуль хранится в большом двоичном объекте Azure в учетной записи хранения с именем contosostorage и контейнером с именем modules.</span><span class="sxs-lookup"><span data-stu-id="9ed90-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="9ed90-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ed90-119">PARAMETERS</span></span>

### <span data-ttu-id="9ed90-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9ed90-120">-AutomationAccountName</span></span>
<span data-ttu-id="9ed90-121">Указывает имя учетной записи автоматизации, для которой этот командлет импортирует модуль.</span><span class="sxs-lookup"><span data-stu-id="9ed90-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="9ed90-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="9ed90-122">-ContentLinkUri</span></span>
<span data-ttu-id="9ed90-123">URL-адрес пакета модуля ZIP</span><span class="sxs-lookup"><span data-stu-id="9ed90-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="9ed90-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ed90-124">-DefaultProfile</span></span>
<span data-ttu-id="9ed90-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9ed90-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ed90-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ed90-126">-Name</span></span>
<span data-ttu-id="9ed90-127">Указывает имя модуля, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="9ed90-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="9ed90-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ed90-128">-ResourceGroupName</span></span>
<span data-ttu-id="9ed90-129">Указывает имя группы ресурсов, для которой этот командлет импортирует модуль.</span><span class="sxs-lookup"><span data-stu-id="9ed90-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="9ed90-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ed90-130">CommonParameters</span></span>
<span data-ttu-id="9ed90-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ed90-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ed90-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ed90-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ed90-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ed90-133">INPUTS</span></span>

### <span data-ttu-id="9ed90-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9ed90-134">System.String</span></span>

### <span data-ttu-id="9ed90-135">System. URI</span><span class="sxs-lookup"><span data-stu-id="9ed90-135">System.Uri</span></span>

## <span data-ttu-id="9ed90-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ed90-136">OUTPUTS</span></span>

### <span data-ttu-id="9ed90-137">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="9ed90-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="9ed90-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ed90-138">NOTES</span></span>

## <span data-ttu-id="9ed90-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ed90-139">RELATED LINKS</span></span>

[<span data-ttu-id="9ed90-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9ed90-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="9ed90-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9ed90-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="9ed90-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9ed90-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)



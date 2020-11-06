---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: e2de3546f805e006bd7f48e2ee7f95b8f3347544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570136"
---
# <span data-ttu-id="d49f9-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d49f9-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="d49f9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d49f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d49f9-103">Импортирует модуль в автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="d49f9-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d49f9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d49f9-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> -ContentLinkUri <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d49f9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d49f9-105">DESCRIPTION</span></span>
<span data-ttu-id="d49f9-106">Командлет **New-AzureRmAutomationModule** импортирует модуль в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="d49f9-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="d49f9-107">Эта команда принимает сжатый файл с расширением ZIP.</span><span class="sxs-lookup"><span data-stu-id="d49f9-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="d49f9-108">Файл содержит папку, в которую входит файл одного из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="d49f9-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="d49f9-109">модуль wps_2, имеющий расширение имени файла. PSM1 или. dll</span><span class="sxs-lookup"><span data-stu-id="d49f9-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="d49f9-110">манифест модуля wps_2, имеющий расширение имени файла. PSD1</span><span class="sxs-lookup"><span data-stu-id="d49f9-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="d49f9-111">Имя ZIP-файла, имя папки, а также имя файла в папке должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="d49f9-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="d49f9-112">Укажите ZIP-файл, который может получать Access служба автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d49f9-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="d49f9-113">При импорте wps_2ного модуля в автоматизацию с помощью этого командлета или командлета Set-AzureRmAutomationModule операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d49f9-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="d49f9-114">Команда завершает выполнение импорта или завершается неуспешно.</span><span class="sxs-lookup"><span data-stu-id="d49f9-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="d49f9-115">Чтобы проверить, успешно ли она выполнена, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d49f9-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="d49f9-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="d49f9-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="d49f9-117">Установите для свойства **ProvisioningState** значение "успешно".</span><span class="sxs-lookup"><span data-stu-id="d49f9-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="d49f9-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d49f9-118">EXAMPLES</span></span>

### <span data-ttu-id="d49f9-119">Пример 1: импорт модуля</span><span class="sxs-lookup"><span data-stu-id="d49f9-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d49f9-120">Эта команда импортирует модуль с именем ContosoModule в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d49f9-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="d49f9-121">Модуль хранится в большом двоичном объекте Azure в учетной записи хранения с именем contosostorage и контейнером с именем modules.</span><span class="sxs-lookup"><span data-stu-id="d49f9-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="d49f9-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d49f9-122">PARAMETERS</span></span>

### <span data-ttu-id="d49f9-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d49f9-123">-AutomationAccountName</span></span>
<span data-ttu-id="d49f9-124">Указывает имя учетной записи автоматизации, для которой этот командлет импортирует модуль.</span><span class="sxs-lookup"><span data-stu-id="d49f9-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="d49f9-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="d49f9-125">-ContentLinkUri</span></span>
<span data-ttu-id="d49f9-126">URL-адрес пакета модуля ZIP.</span><span class="sxs-lookup"><span data-stu-id="d49f9-126">The url to a module zip package.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d49f9-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d49f9-127">-Name</span></span>
<span data-ttu-id="d49f9-128">Указывает имя модуля, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d49f9-128">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="d49f9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d49f9-129">-ResourceGroupName</span></span>
<span data-ttu-id="d49f9-130">Указывает имя группы ресурсов, для которой этот командлет импортирует модуль.</span><span class="sxs-lookup"><span data-stu-id="d49f9-130">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="d49f9-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d49f9-131">-DefaultProfile</span></span>
<span data-ttu-id="d49f9-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d49f9-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d49f9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d49f9-133">CommonParameters</span></span>
<span data-ttu-id="d49f9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d49f9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d49f9-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d49f9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d49f9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d49f9-136">INPUTS</span></span>

## <span data-ttu-id="d49f9-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d49f9-137">OUTPUTS</span></span>

### <span data-ttu-id="d49f9-138">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="d49f9-138">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="d49f9-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="d49f9-139">NOTES</span></span>

## <span data-ttu-id="d49f9-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d49f9-140">RELATED LINKS</span></span>

[<span data-ttu-id="d49f9-141">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d49f9-141">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="d49f9-142">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d49f9-142">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="d49f9-143">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="d49f9-143">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)



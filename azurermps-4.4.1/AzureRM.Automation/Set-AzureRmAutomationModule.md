---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: a0c3693220ab614dcb84d69bc8c17a0ad632a2b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560543"
---
# <span data-ttu-id="debad-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="debad-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="debad-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="debad-102">SYNOPSIS</span></span>
<span data-ttu-id="debad-103">Обновляет модуль в автоматизации.</span><span class="sxs-lookup"><span data-stu-id="debad-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="debad-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="debad-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="debad-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="debad-105">DESCRIPTION</span></span>
<span data-ttu-id="debad-106">Командлет **Set-AzureRmAutomationModule** обновляет модуль в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="debad-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="debad-107">Эта команда принимает сжатый файл с расширением ZIP.</span><span class="sxs-lookup"><span data-stu-id="debad-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="debad-108">Файл содержит папку, в которую входит файл одного из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="debad-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="debad-109">модуль wps_2, имеющий расширение имени файла. PSM1 или. dll</span><span class="sxs-lookup"><span data-stu-id="debad-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="debad-110">манифест модуля wps_2, имеющий расширение имени файла. PSD1</span><span class="sxs-lookup"><span data-stu-id="debad-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="debad-111">Имя ZIP-файла, имя папки, а также имя файла в папке должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="debad-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="debad-112">Укажите ZIP-файл, который может получать Access служба автоматизации.</span><span class="sxs-lookup"><span data-stu-id="debad-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="debad-113">При импорте wps_2ного модуля в автоматизацию с помощью этого командлета или командлета New-AzureRmAutomationModule операция выполняется асинхронно.</span><span class="sxs-lookup"><span data-stu-id="debad-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="debad-114">Команда завершает выполнение импорта или завершается неуспешно.</span><span class="sxs-lookup"><span data-stu-id="debad-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="debad-115">Чтобы проверить, успешно ли она выполнена, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="debad-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="debad-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="debad-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="debad-117">Установите для свойства **ProvisioningState** значение "успешно".</span><span class="sxs-lookup"><span data-stu-id="debad-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="debad-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="debad-118">EXAMPLES</span></span>

### <span data-ttu-id="debad-119">Пример 1: обновление модуля</span><span class="sxs-lookup"><span data-stu-id="debad-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri ".\ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="debad-120">Эта команда импортирует обновленную версию существующего модуля с именем ContosoModule в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="debad-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>

## <span data-ttu-id="debad-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="debad-121">PARAMETERS</span></span>

### <span data-ttu-id="debad-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="debad-122">-AutomationAccountName</span></span>
<span data-ttu-id="debad-123">Указывает имя учетной записи автоматизации, для которой этот командлет обновляет модуль.</span><span class="sxs-lookup"><span data-stu-id="debad-123">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="debad-124">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="debad-124">-ContentLinkUri</span></span>
<span data-ttu-id="debad-125">Задает URL-адрес для файла ZIP, который содержит новую версию модуля, импортируемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="debad-125">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="debad-126">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="debad-126">-ContentLinkVersion</span></span>
<span data-ttu-id="debad-127">Указывает версию модуля, для которого этот командлет обновляет автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="debad-127">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="debad-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="debad-128">-Name</span></span>
<span data-ttu-id="debad-129">Указывает имя модуля, который импортирует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="debad-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="debad-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="debad-130">-ResourceGroupName</span></span>
<span data-ttu-id="debad-131">Указывает имя группы ресурсов, для которой этот командлет обновляет модуль.</span><span class="sxs-lookup"><span data-stu-id="debad-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="debad-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="debad-132">-DefaultProfile</span></span>
<span data-ttu-id="debad-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="debad-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="debad-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="debad-134">CommonParameters</span></span>
<span data-ttu-id="debad-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="debad-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="debad-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="debad-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="debad-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="debad-137">INPUTS</span></span>

## <span data-ttu-id="debad-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="debad-138">OUTPUTS</span></span>

### <span data-ttu-id="debad-139">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="debad-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="debad-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="debad-140">NOTES</span></span>

## <span data-ttu-id="debad-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="debad-141">RELATED LINKS</span></span>

[<span data-ttu-id="debad-142">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="debad-142">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="debad-143">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="debad-143">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="debad-144">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="debad-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418239"
---
# <span data-ttu-id="7b816-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7b816-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="7b816-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b816-102">SYNOPSIS</span></span>
<span data-ttu-id="7b816-103">Обновляет модуль автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7b816-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="7b816-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7b816-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b816-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b816-105">DESCRIPTION</span></span>
<span data-ttu-id="7b816-106">Командлет **Set-AzAutomationModule** обновляет модуль в автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7b816-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="7b816-107">Эта команда принимает сжатый файл с расширением ZIP-файла.</span><span class="sxs-lookup"><span data-stu-id="7b816-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="7b816-108">Файл содержит папку с одним из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="7b816-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="7b816-109">wps_2, который имеет расширение PSM1 или DLL</span><span class="sxs-lookup"><span data-stu-id="7b816-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="7b816-110">wps_2 модуль с расширением PSD1: имя ZIP-файла, имя папки и имя файла в папке должны быть одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="7b816-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="7b816-111">Укажите ZIP-файл как URL-адрес, доступный службе автоматизации.</span><span class="sxs-lookup"><span data-stu-id="7b816-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="7b816-112">Если вы импортируете wps_2 модуля в автоматизацию с помощью этого командлета или New-AzAutomationModule командлета, операция является асинхронной.</span><span class="sxs-lookup"><span data-stu-id="7b816-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="7b816-113">Команда завершает работу независимо от успешного или неудачного завершения импорта.</span><span class="sxs-lookup"><span data-stu-id="7b816-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="7b816-114">Чтобы проверить успешности, запустите следующую команду: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName проверьте свойство **ProvisioningState** на значение "Успешно".</span><span class="sxs-lookup"><span data-stu-id="7b816-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="7b816-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7b816-115">EXAMPLES</span></span>

### <span data-ttu-id="7b816-116">Пример 1. Обновление модуля</span><span class="sxs-lookup"><span data-stu-id="7b816-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7b816-117">Эта команда импортирует обновленную версию существующего модуля ContosoModule в учетную запись автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7b816-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="7b816-118">Модуль хранится в BLOB-проекте Azure в учетной записи хранения contosostorage и контейнере с именами модулей.</span><span class="sxs-lookup"><span data-stu-id="7b816-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="7b816-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b816-119">PARAMETERS</span></span>

### <span data-ttu-id="7b816-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7b816-120">-AutomationAccountName</span></span>
<span data-ttu-id="7b816-121">Указывает имя учетной записи автоматизации, для которой этот командлет обновляет модуль.</span><span class="sxs-lookup"><span data-stu-id="7b816-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="7b816-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="7b816-122">-ContentLinkUri</span></span>
<span data-ttu-id="7b816-123">URL-адрес ZIP-файла, который содержит новую версию модуля, импортируемого этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7b816-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="7b816-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="7b816-124">-ContentLinkVersion</span></span>
<span data-ttu-id="7b816-125">Определяет версию модуля, в которой этот командлет обновляет автоматизацию.</span><span class="sxs-lookup"><span data-stu-id="7b816-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="7b816-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b816-126">-DefaultProfile</span></span>
<span data-ttu-id="7b816-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7b816-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7b816-128">-Name</span><span class="sxs-lookup"><span data-stu-id="7b816-128">-Name</span></span>
<span data-ttu-id="7b816-129">Указывает имя модуля, который импортируется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7b816-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="7b816-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b816-130">-ResourceGroupName</span></span>
<span data-ttu-id="7b816-131">Имя группы ресурсов, для которой этот командлет обновляет модуль.</span><span class="sxs-lookup"><span data-stu-id="7b816-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="7b816-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b816-132">CommonParameters</span></span>
<span data-ttu-id="7b816-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b816-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b816-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b816-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b816-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b816-135">INPUTS</span></span>

### <span data-ttu-id="7b816-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7b816-136">System.String</span></span>

### <span data-ttu-id="7b816-137">System.Uri</span><span class="sxs-lookup"><span data-stu-id="7b816-137">System.Uri</span></span>

## <span data-ttu-id="7b816-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7b816-138">OUTPUTS</span></span>

### <span data-ttu-id="7b816-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="7b816-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="7b816-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7b816-140">NOTES</span></span>

## <span data-ttu-id="7b816-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b816-141">RELATED LINKS</span></span>

[<span data-ttu-id="7b816-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7b816-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="7b816-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7b816-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="7b816-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7b816-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)



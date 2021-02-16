---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235284"
---
# <span data-ttu-id="09770-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="09770-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="09770-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09770-102">SYNOPSIS</span></span>
<span data-ttu-id="09770-103">Получает учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="09770-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="09770-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="09770-104">SYNTAX</span></span>

### <span data-ttu-id="09770-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="09770-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09770-106">ByName</span><span class="sxs-lookup"><span data-stu-id="09770-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09770-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="09770-107">DESCRIPTION</span></span>
<span data-ttu-id="09770-108">**Cmdlet Get-AzAutomationCredential** получает одну или несколько учетных данных автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="09770-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="09770-109">По умолчанию возвращаются все учетные данные.</span><span class="sxs-lookup"><span data-stu-id="09770-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="09770-110">Укажите имя учетных данных для получения определенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="09770-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="09770-111">В целях безопасности этот cmdlet не возвращает пароли учетных данных.</span><span class="sxs-lookup"><span data-stu-id="09770-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="09770-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="09770-112">EXAMPLES</span></span>

### <span data-ttu-id="09770-113">Пример 1. Получить все учетные данные</span><span class="sxs-lookup"><span data-stu-id="09770-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="09770-114">Эта команда получает метаданные для всех учетных данных в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="09770-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="09770-115">Пример 2. Получить учетные данные</span><span class="sxs-lookup"><span data-stu-id="09770-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="09770-116">Эта команда получает метаданные для учетных данных ContosoCredential в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="09770-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="09770-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09770-117">PARAMETERS</span></span>

### <span data-ttu-id="09770-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="09770-118">-AutomationAccountName</span></span>
<span data-ttu-id="09770-119">Указывает имя учетной записи автоматизации, для которой этот cmdlet извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="09770-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="09770-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09770-120">-DefaultProfile</span></span>
<span data-ttu-id="09770-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="09770-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09770-122">-Name</span><span class="sxs-lookup"><span data-stu-id="09770-122">-Name</span></span>
<span data-ttu-id="09770-123">Указывает имя извлечения учетных данных.</span><span class="sxs-lookup"><span data-stu-id="09770-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09770-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09770-124">-ResourceGroupName</span></span>
<span data-ttu-id="09770-125">Определяет группу ресурсов, для которой этот cmdlet извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="09770-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="09770-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09770-126">CommonParameters</span></span>
<span data-ttu-id="09770-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09770-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09770-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09770-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09770-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="09770-129">INPUTS</span></span>

### <span data-ttu-id="09770-130">System.String</span><span class="sxs-lookup"><span data-stu-id="09770-130">System.String</span></span>

## <span data-ttu-id="09770-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="09770-131">OUTPUTS</span></span>

### <span data-ttu-id="09770-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="09770-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="09770-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="09770-133">NOTES</span></span>

## <span data-ttu-id="09770-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="09770-134">RELATED LINKS</span></span>

[<span data-ttu-id="09770-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="09770-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="09770-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="09770-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="09770-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="09770-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072713"
---
# <span data-ttu-id="f84ef-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f84ef-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="f84ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f84ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f84ef-103">Получает учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f84ef-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="f84ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f84ef-104">SYNTAX</span></span>

### <span data-ttu-id="f84ef-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f84ef-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f84ef-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f84ef-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f84ef-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f84ef-107">DESCRIPTION</span></span>
<span data-ttu-id="f84ef-108">Командлет **Get-AzAutomationCredential** получает один или несколько учетных данных службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="f84ef-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="f84ef-109">По умолчанию возвращаются все учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f84ef-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="f84ef-110">Укажите имя учетных данных для получения определенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="f84ef-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="f84ef-111">В целях безопасности этот командлет не возвращает пароли учетных данных.</span><span class="sxs-lookup"><span data-stu-id="f84ef-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="f84ef-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f84ef-112">EXAMPLES</span></span>

### <span data-ttu-id="f84ef-113">Пример 1: получение всех учетных данных</span><span class="sxs-lookup"><span data-stu-id="f84ef-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f84ef-114">Эта команда получает метаданные для всех учетных данных в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f84ef-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="f84ef-115">Пример 2: получение учетных данных</span><span class="sxs-lookup"><span data-stu-id="f84ef-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="f84ef-116">Эта команда получает метаданные для учетных данных с именем ContosoCredential в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="f84ef-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="f84ef-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f84ef-117">PARAMETERS</span></span>

### <span data-ttu-id="f84ef-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f84ef-118">-AutomationAccountName</span></span>
<span data-ttu-id="f84ef-119">Указывает имя учетной записи автоматизации, для которой этот командлет извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f84ef-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="f84ef-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84ef-120">-DefaultProfile</span></span>
<span data-ttu-id="f84ef-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f84ef-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f84ef-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f84ef-122">-Name</span></span>
<span data-ttu-id="f84ef-123">Указывает имя извлекаемых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="f84ef-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="f84ef-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84ef-124">-ResourceGroupName</span></span>
<span data-ttu-id="f84ef-125">Указывает группу ресурсов, для которой этот командлет извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="f84ef-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="f84ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84ef-126">CommonParameters</span></span>
<span data-ttu-id="f84ef-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f84ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84ef-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f84ef-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84ef-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f84ef-129">INPUTS</span></span>

### <span data-ttu-id="f84ef-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f84ef-130">System.String</span></span>

## <span data-ttu-id="f84ef-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f84ef-131">OUTPUTS</span></span>

### <span data-ttu-id="f84ef-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="f84ef-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="f84ef-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="f84ef-133">NOTES</span></span>

## <span data-ttu-id="f84ef-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f84ef-134">RELATED LINKS</span></span>

[<span data-ttu-id="f84ef-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f84ef-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="f84ef-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f84ef-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="f84ef-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f84ef-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3a13605618c5cda3c247cd6b0812732ce018bafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731636"
---
# <span data-ttu-id="1ecb1-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ecb1-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="1ecb1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1ecb1-102">SYNOPSIS</span></span>
<span data-ttu-id="1ecb1-103">Получает учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="1ecb1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1ecb1-104">SYNTAX</span></span>

### <span data-ttu-id="1ecb1-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1ecb1-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1ecb1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="1ecb1-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ecb1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ecb1-107">DESCRIPTION</span></span>
<span data-ttu-id="1ecb1-108">Командлет **Get-AzAutomationCredential** получает один или несколько учетных данных службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="1ecb1-109">По умолчанию возвращаются все учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="1ecb1-110">Укажите имя учетных данных для получения определенных учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="1ecb1-111">В целях безопасности этот командлет не возвращает пароли учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="1ecb1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1ecb1-112">EXAMPLES</span></span>

### <span data-ttu-id="1ecb1-113">Пример 1: получение всех учетных данных</span><span class="sxs-lookup"><span data-stu-id="1ecb1-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1ecb1-114">Эта команда получает метаданные для всех учетных данных в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1ecb1-115">Пример 2: получение учетных данных</span><span class="sxs-lookup"><span data-stu-id="1ecb1-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="1ecb1-116">Эта команда получает метаданные для учетных данных с именем ContosoCredential в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1ecb1-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1ecb1-117">PARAMETERS</span></span>

### <span data-ttu-id="1ecb1-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1ecb1-118">-AutomationAccountName</span></span>
<span data-ttu-id="1ecb1-119">Указывает имя учетной записи автоматизации, для которой этот командлет извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="1ecb1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ecb1-120">-DefaultProfile</span></span>
<span data-ttu-id="1ecb1-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1ecb1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ecb1-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1ecb1-122">-Name</span></span>
<span data-ttu-id="1ecb1-123">Указывает имя извлекаемых учетных данных.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="1ecb1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ecb1-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ecb1-125">Указывает группу ресурсов, для которой этот командлет извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="1ecb1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ecb1-126">CommonParameters</span></span>
<span data-ttu-id="1ecb1-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1ecb1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ecb1-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ecb1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ecb1-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1ecb1-129">INPUTS</span></span>

### <span data-ttu-id="1ecb1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1ecb1-130">System.String</span></span>

## <span data-ttu-id="1ecb1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1ecb1-131">OUTPUTS</span></span>

### <span data-ttu-id="1ecb1-132">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="1ecb1-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="1ecb1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="1ecb1-133">NOTES</span></span>

## <span data-ttu-id="1ecb1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1ecb1-134">RELATED LINKS</span></span>

[<span data-ttu-id="1ecb1-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ecb1-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="1ecb1-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ecb1-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="1ecb1-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="1ecb1-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)



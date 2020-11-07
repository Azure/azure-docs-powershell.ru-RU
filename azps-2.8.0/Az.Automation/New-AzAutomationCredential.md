---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a4d28affaa44e96a713adea7935073bcdf9d93c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727800"
---
# <span data-ttu-id="96d77-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="96d77-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="96d77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96d77-102">SYNOPSIS</span></span>
<span data-ttu-id="96d77-103">Создает учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="96d77-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="96d77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96d77-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96d77-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96d77-105">DESCRIPTION</span></span>
<span data-ttu-id="96d77-106">Командлет **New-AzAutomationCredential** создает учетные данные как объект **PSCredential** в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="96d77-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="96d77-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96d77-107">EXAMPLES</span></span>

### <span data-ttu-id="96d77-108">Пример 1: создание учетных данных</span><span class="sxs-lookup"><span data-stu-id="96d77-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="96d77-109">Первая команда назначает имя пользователя переменной $User.</span><span class="sxs-lookup"><span data-stu-id="96d77-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="96d77-110">Вторая команда преобразует пароль обычного текста в безопасную строку с помощью командлета ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="96d77-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="96d77-111">Команда сохраняет этот объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="96d77-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="96d77-112">Третья команда создает учетные данные на основе $User и $Password, а затем сохраняет их в переменной $Credential.</span><span class="sxs-lookup"><span data-stu-id="96d77-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="96d77-113">Последняя команда создает учетные данные автоматизации с именем ContosoCredential, которая использует $Credential.</span><span class="sxs-lookup"><span data-stu-id="96d77-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="96d77-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96d77-114">PARAMETERS</span></span>

### <span data-ttu-id="96d77-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="96d77-115">-AutomationAccountName</span></span>
<span data-ttu-id="96d77-116">Указывает имя учетной записи автоматизации, в которой этот командлет хранит учетные данные.</span><span class="sxs-lookup"><span data-stu-id="96d77-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="96d77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d77-117">-DefaultProfile</span></span>
<span data-ttu-id="96d77-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="96d77-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96d77-119">-Описание</span><span class="sxs-lookup"><span data-stu-id="96d77-119">-Description</span></span>
<span data-ttu-id="96d77-120">Задает описание учетных данных.</span><span class="sxs-lookup"><span data-stu-id="96d77-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="96d77-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96d77-121">-Name</span></span>
<span data-ttu-id="96d77-122">Задает имя для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="96d77-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="96d77-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d77-123">-ResourceGroupName</span></span>
<span data-ttu-id="96d77-124">Задает описание группы ресурсов, для которой этот командлет создает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="96d77-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="96d77-125">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="96d77-125">-Value</span></span>
<span data-ttu-id="96d77-126">Указывает учетные данные как объект **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="96d77-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96d77-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d77-127">CommonParameters</span></span>
<span data-ttu-id="96d77-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96d77-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d77-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d77-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d77-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96d77-130">INPUTS</span></span>

### <span data-ttu-id="96d77-131">System. String</span><span class="sxs-lookup"><span data-stu-id="96d77-131">System.String</span></span>

### <span data-ttu-id="96d77-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="96d77-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="96d77-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96d77-133">OUTPUTS</span></span>

### <span data-ttu-id="96d77-134">Microsoft. Azure. Commands. Automation. Model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="96d77-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="96d77-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="96d77-135">NOTES</span></span>

## <span data-ttu-id="96d77-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96d77-136">RELATED LINKS</span></span>

[<span data-ttu-id="96d77-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="96d77-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="96d77-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="96d77-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="96d77-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="96d77-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)



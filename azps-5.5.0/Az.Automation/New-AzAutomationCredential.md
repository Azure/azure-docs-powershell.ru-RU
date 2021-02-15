---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100235140"
---
# <span data-ttu-id="94403-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94403-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="94403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94403-102">SYNOPSIS</span></span>
<span data-ttu-id="94403-103">Создает учетные данные автоматизации.</span><span class="sxs-lookup"><span data-stu-id="94403-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="94403-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94403-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="94403-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94403-105">DESCRIPTION</span></span>
<span data-ttu-id="94403-106">Для создания учетных данных **new-AzAutomationCredential** в автоматизации Azure создаются учетные данные в качестве **объекта PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="94403-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="94403-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94403-107">EXAMPLES</span></span>

### <span data-ttu-id="94403-108">Пример 1. Создание учетных данных</span><span class="sxs-lookup"><span data-stu-id="94403-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="94403-109">Первая команда назначает имя пользователя переменной $User.</span><span class="sxs-lookup"><span data-stu-id="94403-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="94403-110">Вторая команда преобразует пароль в виде обычного текста в безопасную строку с помощью ConvertTo-SecureString командлета.</span><span class="sxs-lookup"><span data-stu-id="94403-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="94403-111">Эта команда сохраняет объект в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="94403-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="94403-112">Третья команда создает учетные данные на основе $User и $Password, а затем сохраняет их в $Credential переменной.</span><span class="sxs-lookup"><span data-stu-id="94403-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="94403-113">Конечная команда создает учетные данные автоматизации с именем ContosoCredential, использующие $Credential.</span><span class="sxs-lookup"><span data-stu-id="94403-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="94403-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94403-114">PARAMETERS</span></span>

### <span data-ttu-id="94403-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="94403-115">-AutomationAccountName</span></span>
<span data-ttu-id="94403-116">Указывает имя учетной записи автоматизации, в которой этот cmdlet хранит учетные данные.</span><span class="sxs-lookup"><span data-stu-id="94403-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="94403-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94403-117">-DefaultProfile</span></span>
<span data-ttu-id="94403-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94403-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94403-119">-Description</span><span class="sxs-lookup"><span data-stu-id="94403-119">-Description</span></span>
<span data-ttu-id="94403-120">Описание учетных данных.</span><span class="sxs-lookup"><span data-stu-id="94403-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="94403-121">-Name</span><span class="sxs-lookup"><span data-stu-id="94403-121">-Name</span></span>
<span data-ttu-id="94403-122">Указывает имя учетных данных.</span><span class="sxs-lookup"><span data-stu-id="94403-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="94403-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94403-123">-ResourceGroupName</span></span>
<span data-ttu-id="94403-124">Описание группы ресурсов, для которой этот cmdlet создает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="94403-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="94403-125">-Value</span><span class="sxs-lookup"><span data-stu-id="94403-125">-Value</span></span>
<span data-ttu-id="94403-126">Определяет учетные данные как **объект PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="94403-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="94403-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94403-127">CommonParameters</span></span>
<span data-ttu-id="94403-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94403-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94403-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94403-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94403-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94403-130">INPUTS</span></span>

### <span data-ttu-id="94403-131">System.String</span><span class="sxs-lookup"><span data-stu-id="94403-131">System.String</span></span>

### <span data-ttu-id="94403-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="94403-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="94403-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94403-133">OUTPUTS</span></span>

### <span data-ttu-id="94403-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="94403-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="94403-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94403-135">NOTES</span></span>

## <span data-ttu-id="94403-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94403-136">RELATED LINKS</span></span>

[<span data-ttu-id="94403-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94403-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="94403-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94403-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="94403-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="94403-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


